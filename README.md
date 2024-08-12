Containerized Web Application Deployment with Docker and Docker Compose

Project Overview

🚀 Developed a containerized web application environment using Docker and Docker Compose, featuring WordPress, MySQL, and phpMyAdmin. 

🚀 The project focused on creating Docker images and orchestrating them using Docker Compose to provide a scalable, consistent, and easily deployable setup for web development and database management.

➡️ We are going to create :-

•	Ubuntu based EC2 Instance ( ubuntu 22.04 LTS ).

•	3 Docker container using docker-compose.

     o	MySQL with pre-configured environment variables for database name, user, and password to ensure smooth integration with WordPress.
             
     o	WordPress incorporating necessary PHP extensions and configurations tailored to the project’s needs.
             
     o	phpMyAdmin allowing for easy web-based management of the MySQL database.

Getting Started

✅ Steps: -

•	Launch EC2 Instance with Ubuntu 22.04 LTS OS.  Add the script from enable_ssh_ubuntu22.0 to enable SSH password authentication under User data block while launching the instance.

•	Connect to the instance with SSH.

•	Now use below commands to Install docker and docker-compose using script ubuntu22.0_docker_and_docker_compose_install.sh

      $sudo chmod +x  ubuntu22.0_docker_and_docker_compose_install.sh

      $sh ubuntu22.0_docker_and_docker_compose_install.sh

•	Use the below command to check the docker-compose version.

      $ docker-compose –version

•	Now create docker compose file to create 3 container using docker-compose.yaml

      $docker-compose up -d

      ![image](https://github.com/user-attachments/assets/3027d5ff-fa5a-4aca-86be-57c05ebb8f2e)

 
•	When you hit this command, it actually searches for docker-compose.yaml file in the running directory and it executes all the instructions given in YAML file one by one, it will create container application, network, and volume, based on given instruction in YAML file.

•	Verify containers are created or not using following command

      $docker container ls

      ![image](https://github.com/user-attachments/assets/c1cc4003-1a1c-4639-85ce-7e6abca370a5)


•	Now try to access WordPress URL  Public IP of EC2 :8000

      Setup WordPress username password and you will able to access your WordPress application to design your website.

      ![image](https://github.com/user-attachments/assets/eaece69b-5513-4060-bffd-84d4e782b767)

  

•	Access phpMyAdmin  public IP of EC2 :8080

      MYSQL_USER: my_wp_user

      MYSQL_PASSWORD: my_wp_user_password

      ![image](https://github.com/user-attachments/assets/d9b6f896-0089-4097-9db7-8c3f73151608)


  
