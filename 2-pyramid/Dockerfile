# Use an official Ubuntu base image
FROM ubuntu:latest

# Install necessary utilities
RUN apt-get update && apt-get install -y dos2unix

# Copy the script into the container
COPY pyramid.sh /pyramid.sh

# Convert the script to Unix format
RUN dos2unix /pyramid.sh

# Make the script executable
RUN chmod +x /pyramid.sh

# Use /bin/bash to run the script
ENTRYPOINT ["/bin/bash", "/pyramid.sh"]
