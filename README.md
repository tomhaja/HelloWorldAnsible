# HelloWorldAnsible
Hello World Config Webserver with Ansible



Planung - Erste Notizen
Vorgehen:

User: ubuntu / SSH - Key im Anhang der Mail

1. Repo in git erstellen
- Sign Up: tomhaja/******
- Click Start a Project --> Create a Repo: https://guides.github.com/activities/hello-world/
    - tomhaja/HelloWorldAnsible
    - Add Description
    - use Public
    --> README.md was added

2. Erstellen einer Readme.md --> Dieser Schritt entfällt!

3. Notizen darin speichern.--> Kopieren der Notizen aus Notepad++ to Git 

4. Installation Ansible und HowTo für "Apache config" herraus suchen
    - View Video
    - Windows isn’t supported for the control machine --> Ich verwende eine Azure VM

4.1 Versuch des Deployments einer "Ansible Tower Preconfigured VM"
    - User: toweradmin
    - create ssh key ith puttygen
    - towerc2fnuf4nywi36.westeurope.cloudapp.azure.com
    - Deployment Fails
    - Entscheidung zum Abbruch mit Ansible Tower und hin zu Ubuntu und Selbst installieren via apt

4.2 Deploy Ubuntu
    - take 16.04 LTS
    - ansibleadmin/*****
    - 10.1.0.0/24 - ansiblesub
    - Herrausfinden, wie 'Putty mit sshkeys?
    - Server refused my key.... 
    - 13.80.252.100
    --> Install ansible per https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
    --> install succeeded

4.3 Ansible Playbook
    - https://github.com/ansible/ansible-examples
    - reading  https://www.digitalocean.com/community/tutorials/how-to-configure-apache-using-ansible-on-ubuntu-14-04
    - first config: 
        - creating ansible cfg and hostsfile 
        - testing connection with ping ---> fails because ping is not allowed to  185.128.119.192
        - testing ssh - fails because "Permission denied (publickey)."
    - next ToDo SSH Key am ansible server einrichten --> failed
    - Ergebnis: ssh -i ansiblePrivate.ppk ubuntu@185.128.119.192 -- Enter passphrase for key 'ansiblePrivate.ppk':
        Enter passphrase for key 'ansiblePrivate.ppk':... --> wieso will der hier ein Passwort???

--> 16:51 Abbruch der Versuche eine SSH connection auf 185.128.119.192 zu erstellen


5. Ansible Playbook erstellen, einrichten
    - 17:00 beginn der ansible Configuration 
    - Einrichtung der Files analog dem HowTo:  https://www.digitalocean.com/community/tutorials/how-to-configure-apache-using-ansible-on-ubuntu-14-04

    - Dateien liegen mit im Repo im Ordner "ansible-apache"

6. Hallo world auf Webserver ausgeben --> nicht geschafft

7. Unit Test mit Ansible erstellen --> nicht geschafft

8. Upload der Ansible Konfiguration zu github + Auffrischen(Aussehen und Rechtschreibung) der Dokumentation

9. Undeployment der Testumgebung im AZURE und übersenden der Ergebnisse an Herrn Stephan Pampel
