FROM python:3.8-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

RUN pip3 install evidently

COPY app.py .
COPY model_log_reg.bin .

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=6000"]

