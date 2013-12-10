ansible-user-management
=======================

Ansible role to manage user accounts on hosts

This projects was triggered by a thread in Google groups (https://groups.google.com/forum/#!topic/ansible-project/chJu26GkPlw) and is in its early stage.

Currently, this role looks into the /etc/passwd file and locks all the users that are not available in a users hash of your Ansible inventory. All others get unlocked.

Locking a user means to lock the user's password (usermod --lock USERNAME) and to remove $HOME/.ssh/authorized_keys to also make sure that those users can no longer get access with their private key.
