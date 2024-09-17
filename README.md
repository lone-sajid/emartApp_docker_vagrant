### This project is to deploy Emart Microservices application using docker containers on a Virtual Machine hosted on VMware fusion for Macbook M3 pro using vagrant.

Following are the steps to deploy the application:

Step 1: Clone the repository on your local machine and change to the respective drirectory.

$ git clone git@github.com:lone-sajid/emartApp_docker_vagrant.git

$ cd emartApp_docker_vagrant/MacOSARMChip

Step 2: Now run the below command to build the VM on VMware fusion for which the docker will also get installed using the bootstrap script provided in Vagrantfile.

$ vagrant up

Step 3: Once the VM is up and ready, login to the VM using below ssh command from the directory .../emartApp_docker_vagrant/MacOSARMChip and switch to root user;

$ vagrant up

$ sudo -i

Step 4: Now move to /vagrant/ directory inside VM which will have "emartapp" directory in it. Now cd into this "emartapp" directory which will have "docker-compose.yaml" file;

cd /vagrant/emartapp/

Step 5: Run the below command will be build and depoy the necessary containers on this VM.

docker compose up -d

Step 6: Once everything is up and completed you can use "ip addr show" command to get the IP address of your VM (you can get the IP address information from Vagrantfile directly as well). 
Put the IP in the web browser to see your application being accessible.
