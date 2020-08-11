FROM python:3

RUN ["mkdir", "/project"]

WORKDIR /project

COPY requirements.txt ./

RUN ["pip", "install", "--no-cache-dir", "-r", "requirements.txt"]
