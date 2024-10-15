# Book Catalog Dockerfile

FROM python:3.11-alpine

WORKDIR /book-catalog

COPY /requirements.txt .
# this copies the packages required for the image from the source directory to install to image work directory

RUN pip install --no-cache-dir -r requirements.txt
# this installs the dependencies listed in the packages copied to the work directory

COPY . .
# this copies all the code within the source folder 

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"] 
# this starts the microservice applicable for python