FROM ubuntu:latest

# Avoid prompts during apt operations
ENV DEBIAN_FRONTEND=noninteractive

# Install Python 3 and pip
RUN apt-get update && apt-get install -y python3 python3-pip

# Bypass external management restriction if it exists
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask with pip3
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy your Flask app into the image
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]
