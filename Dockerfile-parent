FROM ubuntu:16.04
RUN apt-get update -y
RUN apt-get install -y software-properties-common 
RUN add-apt-repository universe 
RUN apt-get install -y python-pip python-dev build-essential 
ONBUILD COPY . /app
ONBUILD WORKDIR /app
ONBUILD RUN pip install -r requirements.txt
ONBUILD ENTRYPOINT ["python"]
ONBUILD CMD ["app.py"]
