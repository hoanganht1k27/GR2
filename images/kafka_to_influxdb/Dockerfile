FROM python:3.9.17

WORKDIR /opt
COPY requirements.txt .
COPY main.py .
COPY main_multi_messages.py .

RUN apt-get -y update && \
    apt-get --no-install-recommends -y install dnsutils && \
    apt-get autoclean

RUN pip install --no-cache-dir -r requirements.txt

ENTRYPOINT ["python", "main.py"]