php7-fpm Ansible role
=====================

This role will install php7-fpm in Xenial (16.04)

Requirements
------------

Required packages (installed automatically) :

  - php7-fpm
  - php7.0-opcache
  - php-apcu
  - php7.0-gd
  - php7.0-curl
  - php-pear
  - php7.0-mysql

Role Variables
--------------

  - `php7_memory_limit`: max memory per PHP process (default: 128M)
  - `php7_post_max_size`: max post size (default: 40M)
  - `php7_upload_max_filesize`: max upload size for files (default: 20M)


Tags
----

  - `php7-fpm` : applies to the whole role

Dependencies
------------

  - git@github.com:leucos/ansible-nginx.git

Example Playbook
----------------

This is mainly used as a dependency in your existing playbooks, like:

    dependencies:
      - { role: ansible-php7-fpm }

but can be used in playbooks also :

    - name: web servers
      hosts: webservers
      roles:
        - ansible-php7-fpm

License
-------

MIT

Author Information
------------------

@leucos

