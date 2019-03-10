# docker-jenkins
Docker container for automated builds using jenkins.

docker run -d --restart=always --name jenkins -p 8081:8080 -p 50001:50000 -v /storage/jenkins/:/var/jenkins_home \
   -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker fpotera/jenkins
