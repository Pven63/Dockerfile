# Use the official Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy application source code
COPY . .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the application port (adjust as per Wisecow's default port)
EXPOSE 5000

# Command to run the application
CMD ["python", "app.py"]
