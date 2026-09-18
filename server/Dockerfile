# Add a base image
FROM python:3.9

# Add the requirements.txt file
COPY requirements.txt requirements.txt

# Install and update Python (dependencies)
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Change the working directory
WORKDIR /app

# Copy the rest of the application code
COPY . .

# Expose port
EXPOSE 8000

# Run the command to start the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]