# Set the base image to Ubuntu
FROM python:2.7-stretch

# Metadata indicating an image maintainer.
LABEL maintainer="lorine.zossoungbo@ynov.com"

# Add MongoDB to the repository sources list
ADD ./Projet-Docker/api /Projet-Docker

# Update and install python
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y

# Install motor Flask
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

# Create the data directory
RUN mkdir /dir_data 

# Define to volume
VOLUME /dir_data

# Expose the default port
EXPOSE 5000

# Default port to execute the entrypoint (MongoDB)
CMD [ "python", "./student_age.py" ]



