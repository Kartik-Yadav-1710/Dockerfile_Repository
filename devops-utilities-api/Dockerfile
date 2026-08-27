# Get the base Image
FROM python:3.14

# Get a working directory
WORKDIR  /app

# Get the code In
COPY . . 

# Add the Libraries
RUN pip install -r requirements.txt

# Run the main Application
CMD ["python", "main.py"]



