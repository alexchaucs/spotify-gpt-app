FROM python:latest

# set the working directory
WORKDIR /app

# install dependencies
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --upgrade -r requirements.txt

# copy the scripts to the folder
COPY /src /app/src

# start the server
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "80"]