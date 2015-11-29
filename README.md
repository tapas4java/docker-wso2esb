# docker-wso2esb
===================

Docker Image for WSO2 Enterprise Service Bus(ESB).

The dockerfile will:

* Use `wget` to pull the ESB 4.9.0 ZIP from a S3 bucket into the container `/opt` folder.
* Install `zip`.
* Unzip the ESB 4.9.0 ZIP.
* Remove the ESB 4.9.0 ZIP.
* Expose the container port `9443`.
* Set the ESB `wso2server.sh` start-up script as the container start-up command.

### Usage
* To pull: `docker pull isim/wso2esb`
* To build: `docker build -t wso2-esb github.com/tapas4java/docker-wso2esb`
* To run: `docker run --rm --name your_container_name -p 9443:9443 your_image_name`
* To access ESB web admin console, navigate to `https://localhost:9443`