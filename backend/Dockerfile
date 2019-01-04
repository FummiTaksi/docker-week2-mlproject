FROM python:3.6.7-slim


WORKDIR /src
EXPOSE 5000
COPY . /src

RUN pip install --trusted-host pypi.python.org -r requirements.txt

CMD ["python", "-u", "app.py"]