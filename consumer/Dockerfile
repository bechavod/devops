FROM python:2.7-onbuild
ENV PYTHONPATH /usr/src/app
#ADD consumer/requirements.txt /app
COPY requirements.txt ./usr/src/app/requirements.txt
#ADD consumer/consumer.py ./usr/src/app/
COPY consumer.py ./usr/src/app/consumer.py
WORKDIR /usr/src/app
RUN pip install -r /usr/src/app/requirements.txt
COPY . ./usr/src/app
CMD ["python","consumer.py", "-p", "5672", "-s", "rabbitmq"]
