FROM public.ecr.aws/docker/library/python:3.9.15

RUN apt-get update && apt-get install python -y && \
apt-get install -y \
python3-pip -y

RUN pip install aws_request_auth s3fs requests awswrangler pandas pg8000 requests_aws4auth sqlalchemy


COPY "*.py" "/tmp/"

CMD "python3" "/tmp/sample_python_app.py"