Role Name
=========

Роль nginx 

Requirements
------------

Роль для установки и настройки nginx с 2 виртуальными хостами app1 и app2

Role Variables
--------------
**Переменные используемые в роли**  
nginx_path - каталог с nginx. Значение: /etc/nginx  
nginx_sites - каталог с конфигурациями виртуальных хостов. Значение (зависит от nginx_path) "{{ nginx_path }}/sites-available"  
nginx_sites_enable - каталог с активными конфигурациями виртуальных хостов. Значение (зависит от nginx_path) "{{ nginx_path }}/sites-enabled"  
nginx_index - каталог с файлами для виртуальных хостов. Значение /var/www/html  
vhosts - список виртуальных хостов. Значение: 'app1', 'app2'  
week - статическая переменная-список

Example Playbook
----------------

Для использования роли возможно использовать следующий playbook:

```
name: install and configure nginx  
  hosts: all  
  roles:  
  - nginx  
```

License
-------

BSD

Author Information
------------------
__[@asrytikov](https://t.me/asrytikov)__  
 