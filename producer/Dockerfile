FROM python:2.7-onbuild
ENV PYTHONPATH /usr/src/app
COPY requirements.txt /usr/src/app/requirements.txt
COPY producer.py /usr/src/app/producer.py
WORKDIR /usr/src/app
RUN pip install -r /usr/src/app/requirements.txt
COPY . /usr/src/app
CMD ["python","producer.py", "-p", "5672", "-s", "rabbitmq", "-m","'Hello'", "-r", "30"]
