# Ansible-server-tuning

This project contains ansible roles

## Configuration

Please uncomment the role that you want to run in Playbook.yml file. \
And then check the roles directory that you want to run and set your specific variable which is in vars directory. \
Then check your inventories and choose on which group of inventories you want to make changes. \
Notice: On your remote server make a sudoer user and by running ssh-copy-id on your ansible server put your keys on remote server.
Notice: There is two inventory directory which in one of them password are vault.

## Run

For runnig the playbook you can use command below \
 (-i: define inventory file, -l: define group of inventory):

```bash
ansible-playbook -i inventories/host.ini playbook.yml  -l bastion --ask-become-pass -vv
```
