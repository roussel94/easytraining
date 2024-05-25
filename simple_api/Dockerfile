FROM python:3.8-buster

RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y

COPY requirements.txt /

RUN pip install -r requirements.txt

RUN mkdir /data

COPY student_age.json /data

COPY student_age.py /

EXPOSE 5000

CMD ["python", "./student_age.py"]

