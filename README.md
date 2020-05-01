Ansible SSH [![Build Status](https://travis-ci.org/FinalDes/ansible-ssh.svg?branch=master)](https://travis-ci.org/FinalDes/ansible-ssh)
=========

My personal ssh server configurations

Role Variables
--------------

**ansible_user_id:** remote server login ID  
**public_key_path:** public key location on local server
**no_sudo_pass:** run sudo command without password

Example Playbook
----------------

using management machine public key:

``` YAML
  - hosts: servers
    roles:
       - role: ansible-ssh
         public_key_path: "{{ lookup('file', '{{playbook_dir}}/key/ansible.pub') }}"
```

use public key on remote machine:

``` YAML
  - hosts: servers
    roles:
    - role: ansible-ssh
      public_key_path: "http://my-site.com/mysite"
```

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
