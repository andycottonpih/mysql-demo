# mysql-demo

This is an example setup for a mysql-server docker config to use with PiH development environments.  This setup is not intended for production server deployments.

Configuation changes for the container can be made in the .env file.  
Use TAG to set the mysql version, NAME for the container name, PORT to map 3306 to another host port, and MYSQL_ROOT_PASSWORD to set the initial mysql server login.

Configuration changes for the mysql-server application can be made in ./conf/my.cnf.
Available options for my.cnf will depend on the TAG being used.

The data folder is setup to .gitignore *, new datafiles will be created on first start for the container.

To run this application, you will need docker and docker-compose, from a terminal run: "sudo apt install docker docker-compose"
To allow running docker without sudo, run "sudo usermod -aG docker $USER" then exit and restart your terminal.

To start the mysql-server application, navigate to the repo's local directory in a terminal and run: "docker-compose up -d"
