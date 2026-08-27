# Simple Web Application

A minimal [Python Flask] web application used as the demo app.

## Run manually (without Docker)

These steps assume a fresh machine.

1. Select an OS - Ubuntu

2. Update the package index:

   ```bash
   sudo apt-get update
   ```

3. Install Flask (this also pulls in Python 3):

   ```bash
   sudo apt-get install -y python3-flask
   ```

4. Set the Flask app environment variable:

   ```bash
   export FLASK_APP=app.py
   ```

5. Start the application:

   ```bash
   flask run --host=0.0.0.0
   ```

Then open `http://localhost:5000` and `http://localhost:5000/how-are-you` in a browser.

## The Dockerfile

```dockerfile
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


Each instruction mirrors one of the manual steps above — making it easy to see how a Dockerfile is just an automated install script.
