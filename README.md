# CDDemo
This is the demo of the continuous deployment (Concurrently it is version 0.2).

A static website (index.html) is taken as an example to show how to run CD on the aws Tomcat server.
Once a new branch, with the change in index.html, is merged into the master, git will send a "push" request to Jenkins, and Jenkins will checkout the source code of this git repo and build it into a war file. And this war file will be sent to the Tomcat web server for the deployment. Jenkins and Tomcat server are both installed in my AWS EC2 instance.
The index.html can be checked from here, http://13.59.181.21:8080/demo/.

0. Software dependency.
You only need to install git in your local environment.

a) git
(I am using git for windows https://git-for-windows.github.io/)

1. Setup in my AWS EC2 instance.
1) Install Java8, Git, Ant, Jenkins, Tomcat8.

2) 

2. Comparison from version 0.1

1) No need of script file, post-commit or post-merge to trigger the ant build and push to the Tomcat server.

2) Security: no need to expose my aws key file (since Jenkins and Tomcat are both sitting in my AWS EC2 instance).
