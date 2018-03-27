# IBM MobileFirst v8.0 Installation Guide

## Required Softwares
* nodejs@6.0.0
* npm@3.10.10
* ionic@1.7.14
* Cordova@6.1.1
* Gulp
* MobileFirst 8
* mfpdev-cli
* Maven (if developing adapters)
* Java 8 with Environmental Variables

## Installation
Once the nodejs and npm are installed. Download java and setup the environment variables. 
- Open `MobileFirst Platform Developer Kit` folder and run `./run.sh` (Mac/linux) or `run.cmd` (Windows). This will create development server locally. [For more details, Click Here](https://mobilefirstplatform.ibmcloud.com/downloads/)
- Run `npm i -g ionic cordova gulp-cli`. This command will install the softwares on global level.
- Next execute `npm i -g mfpdev-cli`. If your facing issues with this, make sure you install npm with a version of 3.10.10. Otherwise, it keeps throwing errors.

## Setup Guide
Once the required softwares are installed, open the terminal or command prompt.
- Run `npm -v`, `node -v`, `ionic -v`, `cordova -v`, and `java -version` commands. These should output the versions of your installed softwares. If any of the following doesn't output the version, please make sure to reinstall and try the command again.
- Now to create a project, navigate to your desired folder location using cd command in your terminal. Run `ionic create projectName --type ionic1`. This command will create ionic project.
- Change your directory to the created project and Run `ionic cordova platform` which will create `www` folder. It will also display the available or installed platforms. If you have none, create a Android or iOS platform using `ionic cordova platform add ios@latest` or `ionic cordova platform add android@latest`
- Next, add mfp plugin to the project using `ionic cordova plugin add cordova-plugin-mfp`. With this we can integrate IBM MobileFirst Platform Foundation capabilities to our existing Cordova application. To make sure, it's installed you could run `ionic plugin ls` which will list all the plugins integrated with the project.
- To make sure, your server is up and running. Run `mfpdev server info`. This will show all the mfp server running in your system.
- Run `mfpdev app register` to register the application we initiated in the server for android or iOS platform. Open your browser and navigate to `localhost:9080/mfpconsole` to access MobileFirst Platform console. You should see the application you registered.
- To preview the app, run `mfpdev app preview`, then select the platform you want to preview ther app. This will open the look and feel of the app in browser or the phone simulator.

## Knowledge
- IBM MobileFirst Platform adapters act as a middleware between MFP Server and the Backend.


## Feedback
Please report any bugs or issues in the GitHub issues section. Thank you and I hope this guide helped you.
