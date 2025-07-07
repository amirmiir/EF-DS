FROM python:3.9-slim

WORKDIR /usr/bin/legacy-app
COPY ./requirements.txt ./
RUN pip install -r requirements.txt

COPY ./legacy-app.py .
CMD ["python3", "legacy-app.py"]
