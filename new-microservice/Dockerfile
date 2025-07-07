FROM alpine:latest

ENV PYTHONUNBUFFERED=1
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
COPY ./new-app.py .
CMD ["python3", "new-app.py"]