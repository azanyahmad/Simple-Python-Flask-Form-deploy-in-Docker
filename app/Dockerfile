# Use a base Python image
FROM python:3.8

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt file into the container
COPY requirements.txt /app/

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Flask application code into the container
COPY . /build/

# Expose the port your Flask app runs on (change 3000 to the actual port if needed)
EXPOSE 5000

# Start the Flask app
CMD ["python", "app.py"]