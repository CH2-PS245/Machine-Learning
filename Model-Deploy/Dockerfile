FROM python:3.11.3

# allow statements and log messages to immediately appear in the Knative logs.
ENV PYTHONUNBUFFERED True

# copy local code to the container image.
WORKDIR /app
COPY . .

# install production dependencies.
RUN pip install Flask gunicorn

RUN pip install -r requirements.txt

RUN pip install --upgrade pip

COPY requirements.txt requirements.txt

EXPOSE 8080

CMD [ "python", "app.py" ]
