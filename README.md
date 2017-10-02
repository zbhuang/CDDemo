# CDDemo
This is the demo of the continuous deployment (Concurrently it is version 0.1).

A static website (index.html) is taken as an example to show how to run CD on the aws Tomcat server.
Once the change is committed to the index.html file, "ant" will wrap up this static web app into a demo.war file.
Then this war file will be pushed to my aws Tomcat server (for hot deployment).
The result can be checked from here, http://18.221.214.173:8080/demo/

0. Software dependency.
You need to install git, ant, java.

a) git
(I am using git for windows https://git-for-windows.github.io/)

b) Java - please check this webiste for the installation - 
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html.
(I am using Java8)

c) Apache Ant - download it and unzip it to your local disk and add it to your system environment.
In my case, windows, I add its bin folder to the env, Path.

1. Copy post-merge to this project's .git\hooks folder
After you pull this project, there will be .git\hooks folder, which is hidden, in this project directory.
Move this post-merge file to that hooks folder.
Note you need to give the execute permission to that post-commit file.

2. You can make the change to the index.html file (for example, update that counter).
Once you merge your change to the master branch, a demo.war will be generated.
The it will be uploaded to the Tomcat8 server for the hot deployment (in my aws account).
You can check the change in that counter here, http://18.221.214.173:8080/demo/.

3. 
