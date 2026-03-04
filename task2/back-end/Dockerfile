FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

# Install python and pip
RUN apt-get install -y python3 python3-pip

# Remove externally managed restriction (AlmaLinux compatibility)
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install flask using pip3
RUN pip3 install flask

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python3", "api.py"]
