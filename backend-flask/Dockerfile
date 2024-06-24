FROM python:3.10-slim-buster

# Inside the Container
# Make the New Folder inside the Container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# This contain the LIBRARIES you want to install to run the App
COPY requirements.txt requirements.txt

# Inside Container
# Install the Python Libraries Used for the App
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means everything in the Current Directory
# first period . - /backend-flask (outside container)
# second period . - /backend-flask (inside container)
COPY . .

# Set the Environment Variable(Env Vars)
# Inside Container and will remain Set when the Container is Running
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD stands for (Command):
# python3 -m flask run --host=0.0.0.0 --port =4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]