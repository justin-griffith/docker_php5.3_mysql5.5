To initialize:
	1. Check out the repo
	2. Navigate to the directory where the docker-compose.yml resides
	3. Add your mysql dump, html files etc
	4. run 'docker-compose up -d'

To access the web server visit 
	https://localhost:8443 for SSL
	http://localhost:8080 for no SSL.

To access phpMyadmin: 
	http://localhost:8004/

Attach to the container by running: 
	sudo docker exec -i -t "your container id" /bin/bash

For Windows and Mac substitute localhost with the IP of your docker.

SSH Credentials:
	User: root
	Pass: password
	(ssh root@localhost -p 8022 (Use password: password)

You can connect to mysql using:
	mysql -h 127.0.0.1 -P 9906 -u <userdefined in docker-compose.yml> -p


Put your web code in html directory on your local and it will also be located in the docker container at /var/www/html.

Put additional configuration or setup files within setup_files, they will live at /var/www/config in the webserver container
