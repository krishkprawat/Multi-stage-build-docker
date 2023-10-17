FROM ubuntu AS Build

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    cd devops

#ENTRYPOINT ["python3"]
#CMD ["manage.py", "runserver", "0.0.0.0:8000"]


#==================================
#=====================here starts stage 2 =========
 # this is distroless image of python.
FROM gcr.io/distroless/python3  

COPY --from=Build  /app /app
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]


 







