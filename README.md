# Week2_CI-CD_tools

### 1. Create Jenkins VM with internet access:

* install openjdk-8-jdk or openjdk-11-jdk, Git:

    `apt search openjdk`
    
    `apt-get install -y openjdk-11-jdk git`
    
    <img width="772" alt="Screenshot 2021-10-15 at 08 37 29" src="https://user-images.githubusercontent.com/26361903/137437725-f3644203-75ba-4262-a7c2-46fff7fcea05.png">

* install Jenkins with enabling autostart on startup:

    ```
    wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
    sudo apt-get update
    sudo add-apt-repository universe
    sudo apt-get install jenkins
    systemctl status jenkins
    ```
    <img width="986" alt="Screenshot 2021-10-15 at 08 45 24" src="https://user-images.githubusercontent.com/26361903/137438493-3be01686-e0cc-48d5-a383-1419845771be.png">

* setup custom port 8081 for Jenkins:

    `vi /etc/jenkins/default`
    
    <img width="530" alt="Screenshot 2021-10-15 at 08 51 40" src="https://user-images.githubusercontent.com/26361903/137439010-916292b3-5fa4-4352-8ae5-34638589868d.png">

    `systemctl restart jenkins`
    
* plugins – select plugins, add GitHub and Role-based authorization strategy:

    <img width="1425" alt="Screenshot 2021-10-15 at 09 04 57" src="https://user-images.githubusercontent.com/26361903/137440157-75ba1472-63f6-4cad-8f92-03da73d6351a.png">

    <img width="1436" alt="Screenshot 2021-10-15 at 09 06 30" src="https://user-images.githubusercontent.com/26361903/137440258-857ccf46-a3ac-4dea-9033-9a197cf7600a.png">




