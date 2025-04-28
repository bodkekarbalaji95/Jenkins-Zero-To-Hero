# Use Python base image
FROM python:3.13

# Set working directory
WORKDIR /app

# Copy application files
COPY . .

# Install system dependencies and distutils
RUN apt-get update && apt-get install -y python3-distutils

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Run migrations
RUN python manage.py migrate
