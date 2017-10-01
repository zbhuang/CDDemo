# CDDemo
This is the demo of the continuous deployment (Concurrently it is version 0.1).

Once the change is committed to the index.html file, ant will wrap up this static web app into a demo.war file.
Then this war file will be pushed to my aws Tomcat server (for hot deployment).
The result can be checked from here, http://18.221.214.173:8080/demo/

0. Software dependency.
You need to install git, ant, java (I am using Java8)

1. Copy post-commit to this project's .git\hooks folder
After you pull this project, there will be .git\hooks folder, which is hidden.
Move this post-commit file to that hooks folder.
Note you need to give the execute permission to that post-commit file.

2. You can make the change to the index.html file.
Once you commit your change of index.html, a demo.war will be generated.
The it will be uploaded to the Tomcat8 server for the hot deployment (in my aws account).

3. 
