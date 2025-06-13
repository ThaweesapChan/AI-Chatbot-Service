# Use official Python image
FROM python:3.11

# Set work directory
WORKDIR /app

# Copy all source code
COPY . .

# Install dependencies
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Expose the port Cloud Run expects
EXPOSE 8080

# Run the Django app using Gunicorn
CMD ["gunicorn", "--bind", "0.0.0.0:8080", "chatbot_backend.wsgi:application"]
