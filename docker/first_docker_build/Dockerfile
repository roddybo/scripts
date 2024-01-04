
# Use the Alpine Linux base image
FROM alpine:latest

# Update the package repository and install a sample package (e.g., curl)
RUN apk update && \
    apk add curl

# vim or nano: Text editors for editing files inside the container
RUN apk add --no-cache bash vim

# A syslog daemon for logging
RUN apk add --no-cache curl wget htop

# net-tools: Includes common networking tools like ifconfig and netstat
RUN apk add --no-cache openssl net-tools

# tzdata package and set the timezone
RUN apk add --no-cache tzdata
ENV TZ=America/Los_Angeles

# Update the package repository and install tini
RUN apk update && \
    apk add tini

# Run a loop to keep the container running
CMD ["sh", "-c", "while true; do echo 'Container is running...'; sleep 1; done"]

