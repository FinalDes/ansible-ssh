Ansible SSH
=========

My personal ssh server configurations

Role Variables
--------------

ansible_user_id: remote server login ID
public_key_path: public key location on local server


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: ansible-ssh
           ansible_user_id: ansible
           public_key_path: /User/ansible/.ssh/ansible.pub

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
