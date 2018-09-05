# HelloWorldAnsible
Hello World Config Webserver with Ansible



Planung - Erste Notizen
Vorgehen:

User: ubuntu / SSH - Key im Anhang der Mail

1. Repo in git erstellen
- Sign Up: tomhaja/******
- Start a Project
- Create Repo: nach https://guides.github.com/activities/hello-world/
-  tomhaja/HelloWorldAnsible
- Add Description
- use Public
--> README.md was added

2. Readme.md anlegen --> Dieser Schritt entfällt!
3. Notizen darin speichern.--> Copy Notes from Notepad++ to Git 

4. Was ist Ansible? - How to für Apache config raussuchen
- View Video
- Windows isn’t supported for the control machine --> Use Azure to Deploy vm
- use Ansible Tower Preconfigured VM: User: toweradmin
- create ssh key ith puttygen
- towerc2fnuf4nywi36.westeurope.cloudapp.azure.com
- Deployment Fails
- Retry und deploy Ubuntu
- take 16.04 LTS
- ansibleadmin/*****
10.1.0.0/24 - ansiblesub
- how to use Putty with keys?
- Server refused my key.... 
- Entscheidung zum Abbruch mit Ansible Tower und hin zu ubuntu und selbstinstallation
-13.80.252.100
--> Install ansible per https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
--> install succeeded
- Ansible Playbooks: https://github.com/ansible/ansible-examples
reading  https://www.digitalocean.com/community/tutorials/how-to-configure-apache-using-ansible-on-ubuntu-14-04
- first config: 
    - creating ansible cfg and hostsfile 
    - testing connection with ping ---> fails because ping is not allowed to  185.128.119.192
    - testing ssh - fails because "Permission denied (publickey)."
- next ToDo SSH Key am ansible server einrichten --> failed
ssh -i ansiblePrivate.ppk ubuntu@185.128.119.192 -- Enter passphrase for key 'ansiblePrivate.ppk':
Enter passphrase for key 'ansiblePrivate.ppk':
Enter passphrase for key 'ansiblePrivate.ppk':
Permission denied (publickey).
wieso will der hier ein Passwort???

--> 16:51 Abbruch der Versuche eine SSH connection auf 185.128.119.192 zu erstellen

5. Ansible Playbook erstellen, einrichten
17:00 beginn der ansible Configuration 


6. Hallo world auf Webserver ausgeben --> nicht geschafft
7. Unit Test mit Ansible erstellen --> nicht geschafft

8. Download der Configuration + Auffrischen(Aussehen und Rechtschreibung) der Dokumentation
