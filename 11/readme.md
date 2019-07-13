server_install.yml - playbook для развертывания freeipa-сервера.

client_install.yml - playbook для развертывания freeipa-клиента.

Оба плейбука проверяют, есть ли /etc/ipa/default.conf и, если нет, производят конфигурирование.

server_install.yml выдавал ошибку на этапе ipa-server-install при запуске на ВМ с ОЗУ<2048.


После добавления в /etc/hosts на рабочей машине имени развернутого сервера удалось попасть и посмотреть на интерфейс администратора freeipa.
