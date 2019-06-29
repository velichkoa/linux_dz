# H1 1. Запретить всем пользователям, кроме группы admin логин в выходные и праздничные дни

Созданы пользователи: User1, User2 (-g admin), User3 (-g admin), User4. Пароли: Otusadmin2019 (для группы admin), Otus2019 (для остальных).
Воспользовался модулем pam_exec, прописав его в /etc/pam.d/sshd с типом auth. Исполняемый скрипт: /usr/local/bin/pamscriptlogin.sh, праздничные даты перечисляются в /var/holidays.

# H1 2. Дать конкретному пользователю права рута

Для пользователя User4 создана запись в sudoers:
echo 'User4 ALL=(ALL) NOPASSWD: ALL'>/etc/sudoers.d/User4

