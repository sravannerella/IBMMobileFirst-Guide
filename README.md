# IBM MobileFirst v8.0 Installation Guide

## Required Softwares
* nodejs
* npm@3.10.10
* ionic
* Cordova
* Gulp
* mfpdev-cli
* Maven (if developing adapters)
* Java 8 with Environmental Variables

## Installation
Once the nodejs and npm are installed. Download java and setup the environment variables. 
- Run `npm i -g ionic cordova gulp-cli`. This command will install the softwares on global level.
- Next execute `npm i -g mfpdev-cli`. If your facing issues with this, make sure you install npm with a version of 3.10.10. Otherwise, it keeps throwing errors.
 
## Setup Guide
Once the required softwares are installed, open the terminal or command prompt.
- Run `npm -v`, `node -v`, `ionic -v`, `cordova -v`, and `java -version` commands. These should output the versions of your installed softwares. If any of the following doesn't output the version, please make sure to reinstall and try the command again.
- Now to create a project, navigate to your desired folder location using cd command in your terminal. Run `ionic create projectName`. This command will create ionic project.
- Change your directory to the created project and Run `ionic cordova platform` which will create `www` folder. It will also display the available or installed platforms. If you have none, create a Android or iOS platform using `ionic cordova platform add ios@latest` or `ionic cordova platform add android@latest`
- Next, add mfp plugin to the project using `ionic plugin add cordova-plugin-mfp`. With this we can integrate IBM MobileFirst Platform Foundation capabilities to our existing Cordova application. To make sure, it's installed you could run `ionic plugin ls` which will list all the plugins integrated with the project.

## Feedback
Please report any bugs or issues in the GitHub issues section. Thank you and I hope this guide helped you.
