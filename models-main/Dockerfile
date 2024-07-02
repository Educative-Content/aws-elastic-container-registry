FROM ubuntu:latest

# Update package list and install required packages
RUN apt-get update && apt-get install -y python3-pip python3-venv

# Create a virtual environment and activate it
RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"

# Install Flask inside the virtual environment
RUN pip install flask

# Copy your application code
COPY echo.py echo.py

# Set the entrypoint to use the Python executable from the virtual environment
ENTRYPOINT ["/opt/venv/bin/python", "echo.py"]
