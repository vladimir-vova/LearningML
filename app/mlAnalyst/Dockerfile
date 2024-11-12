FROM python:3.10-slim-buster

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY eda.py ./
COPY model.py ./
COPY app.py ./

RUN python eda.py
RUN python model.py

EXPOSE 5000
CMD ["python", "./app.py"]
