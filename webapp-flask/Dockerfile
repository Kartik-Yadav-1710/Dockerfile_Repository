# Get the Base Image
FROM python:3.12-slim

# Get the working directory
WORKDIR /app

# Get the source code
COPY . .

# Add the Libraries
RUN pip install -r requirements.txt

# Run the main Application
CMD ["python", "app.py"]

