#File to set up and run a Jenkins instance with Docker Compose
version: '3.8'

services:
  jenkins:
    image: jenkins/jenkins:lts
    container_name: jenkins
    ports:
      - "8080:8080"  # Jenkins Web UI
      - "50000:50000"  # Jenkins Agent
    volumes:
      - jenkins_home:/var/jenkins_home  # Persistent Jenkins data
    restart: unless-stopped  # Automatically restart the container if it stops

volumes:
  jenkins_home:
    driver: local
Steps to Use the Docker Compose File
Create a Directory for Jenkins Compose Setup:



mkdir jenkins-docker-compose
cd jenkins-docker-compose
Save the Compose File: Create a file named docker-compose.yml in the directory and paste the content above.

Start the Jenkins Container: Run the following command to start the Jenkins container:



docker-compose up -d
Check the Running Container: Verify that the Jenkins container is running:



docker ps
Retrieve the Initial Admin Password: Get the initial admin password to unlock Jenkins:



docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
Access Jenkins:

Open a browser and navigate to:
arduino

http://localhost:8080
Enter the initial admin password when prompted.
Stop the Jenkins Container: If you need to stop the Jenkins container:



docker-compose down
###########################################
