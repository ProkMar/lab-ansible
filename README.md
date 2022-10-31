# lab-ansible
Лабораторная работа по ansible

Домашнее задание
Настроить виртуальную машину на Yandex Cloud при помощи Ansible

Цель:
В результате домашнего задания, вы научитесь создавать конфигурацию для автоматизации развёртывания при помощи Ansible и установите необходимый софт на свою виртуальную машину в Yandex.Cloud'е


Описание/Пошаговая инструкция выполнения домашнего задания:
Установить себе на рабочий компьютер Ansible
Создать playbook для установки и запуска nginx и postgres на виртуальной машине

## Реализация
Установка nginx и posgres реализована в разных файлах:
    * install_nginx.yml
    * install_postgres.yml

Каждый из них может быть настроен на установку на отдельной или одной
и тоже машины.

### Примеры проверки:
    * ansible-playbook -KC install_nginx.yml -i <your path>/lab-ansible/playbook/hosts.ini
    * ansible-playbook -KC install_postgres.yml -i <your path>/lab-ansible/playbook/hosts.ini   

### Примеры запуска:
    * ansible-playbook -K install_nginx.yml -i <your path>/lab-ansible/playbook/hosts.ini
    * ansible-playbook -K install_postgres.yml -i <your path>/lab-ansible/playbook/hosts.ini

После выполнения плейбуков обращение по адресу виртуальной машины по http выдает текст:
# nginx, configured by Ansible
If you can see this, Ansible successfully installed nginx.

Ansible managed


а к серверу postgres можно подключиться клиентом, например DBeaver.
