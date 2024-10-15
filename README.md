# OTUS PRO Homework 09-NFS

### Домашняя работа 09: NFS и FUSE

### 1) Зайдите на OS, где установлен Ansible с root доступом
   - Примечание: используйте пользователя **root** либо команды: **su - root** либо **sudo -i**

### 2) Выполните данную команду на удаленной машине:
```
apt update -y && apt install git -y ; git clone https://github.com/avlikh/Otus_pro_09.git /ansible;
```
### 3) Внесите изменения в файл: /ansible/vars/vars_file.yml
   - имя и ip-адрес nfs сервера
   - имя и ip-адрес nfs клиента
   - название nfs-папок на сервере и на клиенте  
  
   - Примечание: В данном ДЗ я не использовал файл-hosts, хотя и знаю что его рекомендуется использовать. Захотелось разобраться как можно добавить хосты с импользованием пременных. Получилось...

### 4) Выполните данную команду на удаленной машине. Будет запущен playbook, который настроит nfs-сервер и nfs-клиент.
```
cd /ansible/ && ansible-playbook /ansible/nfs.yaml -u root --ask-pass;
```
   - Вам потребуется ввести пароль пользователя root для подключения Ansible к удаленной машине (я не использовал rsa-ключи, что бы облегчить Вам прием этого ДЗ) 

