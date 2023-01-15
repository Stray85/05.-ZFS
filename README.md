Vagrant-стенд для обновления ядра и создания образа системы

Просмотр версии ядра:
uname -r
Просмотр каталога с ядрами boot:
ll /boot
Установка репозитория 
sudo rpm -Uvh https://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm
Выводим список доступных ядер:
yum list available --disablerepo='*' --enablerepo=elrepo-kernel
Устанавливаем последнее ядро долгосрочной поддержки:
sudo yum --enablerepo=elrepo-kernel install kernel-lt
Перезагрузка и проверка версии.
