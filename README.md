# OTUS-LAB-6
 Управление пакетами. Дистрибьюция софта.
 
Для усложнения задачи решил собрать из исходников "clogtails" Александра Румянцева deb-пакет, и сделать свой репо на nginx.
Для создания репо использовался reprepro. Задача чисто синтетическая, и не имеет практической ценности в моем случае.

Адрес репозитория: http://35.192.231.41/

Использование на сторонней машине:

vim /etc/apt/sources.list

  deb http://35.192.231.41/debian/ testing main contrib

wget -O - -q http://35.192.231.41/otus.gpg.key | apt-key add -
apt-get update
apt-get install clogtail

root@node-1:~# dpkg -l |grep clogta

ii  clogtail                              0.3-1                             amd64        Log follower for periodic jobs
