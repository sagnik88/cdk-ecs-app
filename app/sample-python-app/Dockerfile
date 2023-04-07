FROM public.ecr.aws/docker/library/python:3.9.15

#ARG AWS_ACCESS_KEY_ID
#ARG AWS_SECRET_ACCESS_KEY
#ARG AWS_DEFAULT_REGION
#
#ENV AWS_ACCESS_KEY_ID ${AWS_ACCESS_KEY_ID}
#ENV AWS_SECRET_ACCESS_KEY ${AWS_SECRET_ACCESS_KEY}
#ENV AWS_DEFAULT_REGION ${AWS_DEFAULT_REGION}

RUN apt-get update && apt-get install python -y && \
        apt-get install -y \
              python3-pip -y
RUN pip install aws_requests_auth s3fs requests awswrangler pandas pg8000 requests_aws4auth sqlalchemy
#RUN pip install aws_requests_auth==0.4.3
#RUN pip install requests==2.28.2
#RUN pip install awswrangler==2.19.0
#RUN pip install pandas==1.5.1
#RUN pip install pg8000==1.29.4
#RUN pip install s3fs==2023.1.0
#RUN pip install requests_aws4auth==1.2.2
#RUN pip install sqlalchemy==2.0.3
COPY "*.py" "/tmp/"

CMD "python3" "/tmp/sample_python_app.py"
