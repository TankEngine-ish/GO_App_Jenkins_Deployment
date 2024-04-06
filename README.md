# GO_WebApp_Deployment

# Introduction

This simple web app was my first ever CI/CD Pipeline in Jenkins. It was a steep learning curve because I employed a lot of technologies,
plenty of plugins and a bit of my own personal ideas to make it all a bit more challenging.

# VIDEO

This is my second video for my sequence of DevOps projects in which I go through my process:


## System Set-Up

Once again I've decided to experiment from the get-go and installed Jenkins on a `WSL instance of Ubuntu` on top of my `Windows Homelab`.

## Jenkins Set-Up

* I installed openJDK 11 which is the open-source implementation of version 11 of the Java SE Platform.

* Then I added the Jenkins repo to my system and after that I had to import the GPG keys from Jenkins site to verify the integrity of my packages.

* I followed up with actually installing Jenkins and getting a username and a password.

## Writing the Multi-Stage Pipeline

* I specified the Test, Build and Run stages which of course do not directly correspond to Dev, Stage and Run in a typical SDLC scenario but it's a start.

![jenkinsfile](public/31321321.png)











# Other important things I've learned

- Artifacts in Jenkins
- The potential of using Prometheus for monitoring the pipelines
- The purpose of incremental builds to build only the necessary parts of a project
- The difference between polling and push webhooks in doing a build
- The importance of Authentication (security realm) and Authorization (permissions) and configuring Matrix-Based Authorization Strategies