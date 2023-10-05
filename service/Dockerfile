FROM python:3.11

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

COPY py-common/ py-common/
RUN pip install ./py-common

COPY service/requirements.txt requirements.txt
RUN pip install -r requirements.txt

WORKDIR app/
COPY service/ .

CMD ["python", "main.py"]