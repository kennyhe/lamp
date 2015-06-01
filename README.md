#LAMP stack, with SSH server. (Based on the tutum one.)

##Run
docker run --name lamp -t -i -p 80:80 -p 2200:22 -p 23306:3306 -v ~/www:/var/www/html hekenny/lamp /bin/bash

After the container starts, start the services in the interactive mode:
1. Start the SSHD:
service ssh start
2. Start the LAMP stack
/run.sh  &
3. Run MySql client, create DB and users, and grant permissions.

Then you can use the tools on the host machine to access the MySql to create database, and put your PHP code and files under ~/www folder of your host.
