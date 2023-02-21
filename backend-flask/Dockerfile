FROM python:3.10-slim-buster

#Inside container
#makes a new folder inside container
WORKDIR /backend-flask
#outside container -> Inside container
# contains the libaries we want to install to run the app
COPY requirements.txt requirements.txt
#inside container
#install the python libaries used for app
RUN pip3 install -r requirements.txt

#outside container
#means everuthing in the current directory
#first period -/backen flask(outside container)
#second period ./backend-flask(inside container)
COPY . .
#set env variables(env var)
#inside container and will remain set when container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}
#CMD
#cmd
#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]