### RAID

Делал дз с одной *. С ** буду ковыряться по возможности.
В vagrantfile добавлены 8 новых дисков (указан абсолютный Windows-путь) и строка [mdadm --create --verbose /dev/md0 -l 10 -n 8 /dev/sd{b,c,d,e,f,g,h,i}] в box.vm.provision.
При "vagrant up" собрался Raid10 из 2 секций по 4 диска. 
Далее по методичке записал mdadm.conf и поигрался с mdadm и parted. 
Оставил неразмеченным и вне Raid девятый созданный диск /dev/sdj для последующих опытов.
