FROM continuumio/miniconda3
WORKDIR /app
COPY 1.sh /app
RUN chmod +x /app/1.sh
EXPOSE 3000
RUN pip install boto3 mlflow pymysql
CMD [ "/app/1.sh" ]