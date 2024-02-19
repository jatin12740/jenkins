#Installation
Update Package List:
sudo apt-get update

Install Java:
Jenkins requires Java to run. You can install OpenJDK with the following command:
sudo apt-get install openjdk-11-jdk

Add Jenkins Repository Key:
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo gpg --dearmor -o /usr/share/keyrings/jenkins-keyring.gpg

Add Jenkins Repository:
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.gpg] https://pkg.jenkins.io/debian-stable binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

Update Package List Again:
sudo apt-get update

Install Jenkins:
sudo apt-get install jenkins

Start Jenkins Service:
sudo systemctl start jenkins

Enable Jenkins to Start on Boot:
sudo systemctl enable jenkins

Check Jenkins Status:
sudo systemctl status jenkins

This command will show you whether Jenkins is active and running.

Open Jenkins in your Browser:

    Open your web browser and go to http://localhost:8080 (or the server's IP address or domain name if Jenkins is installed on a remote server).
    Follow the instructions to unlock Jenkins. You can find the initial admin password in the Jenkins server logs or in the file /var/lib/jenkins/secrets/initialAdminPassword. Use the following command to view the password:

    sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Continue Jenkins Setup:

    Follow the on-screen instructions to complete the setup by installing recommended plugins and creating an admin user.
