# Lendable Test Project
## Prerequisites
- Ansible
## Deployment
The instruction here are meant to replicate the same results for any number of similar ec2 servers
- check out the code to a new folder and go into the new folder
- run the command below replacing the private key to the location of your private key

```
ansible-playbook -T 60 -f 100 --private-key=~/user.pem -i hosts.ini deploy.yml
```
### To add more hosts
Add the hosts to the hosts.ini file in the format shown for the existing server