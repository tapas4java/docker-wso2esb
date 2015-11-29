docker-wso2esb
==============

Docker Image for WSO2 Enterprise Service Bus(ESB).

The dockerfile will:

* Copy `4.9.0 zip` to /otp from Packages directory.
* Unzip the ESB 4.9.0 ZIP.
* Remove the ESB 4.9.0 ZIP.
* Expose the container port `9443`.
* Set the ESB `wso2server.sh` start-up script as the container start-up command.

### Usage
* To pull: `docker pull anitech/wso2-esb`
* To build: `docker build -t your_image_name github.com/tapas4java/docker-wso2esb`
* To run: `docker run --rm --name your_container_name -p 9443:9443 your_image_name`
* To access ESB web admin console, navigate to `https://localhost:9443`