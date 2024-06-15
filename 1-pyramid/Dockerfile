# Comments are made with the pound sign

FROM  ubuntu:latest
RUN   sudo apt-get update && apt-get install docs2unix  
COPY  ./pyramid.sh  /pyramid.sh
RUN   docs2unix /pyramid
RUN   chmod +x /pyramid.sh
CMD   ["/pyramid.sh"]


FROM ubuntu:latest

# Install necessary utilities
RUN apt-get update && apt-get install -y dos2unix

# Copy the script into the container
COPY pyramid.sh /pyramid.sh

# Convert the script to Unix format
RUN dos2unix /pyramid.sh

# Make the script executable
RUN chmod +x /pyramid.sh

# Run the script
CMD ["/pyramid.sh"]