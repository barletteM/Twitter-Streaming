FROM python:3.8-alpine3.11
LABEL maintainer="Barlette Makuwe <barlette-m.makuwe@iubh.de>"

RUN apk update && apk add build-base

WORKDIR /produce-tweets
COPY . .

RUN pip install -r requirements.txt

# EXPOSE 8000
# HEALTHCHECK CMD xxx

CMD ["python", "run.py"]