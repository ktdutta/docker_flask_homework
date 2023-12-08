# selecting base image for docker
FROM python:3.7-alpine

# creating a new folder called app and making it the working directory 
WORKDIR /app

# copying files 'app.py', 'Dockerfile','requirements.txt' into the folder app
COPY . /app/

# installing what is inside 'requirements.txt'
RUN pip install -r requirements.txt

# creating container on port 
EXPOSE 5000

# syntax which runs the application 'app.py'
CMD ["python", "app.py"]
