# docker
how to run file in container

1. Create a dockerfile(dockerfile is a text file)
2.(here)
  FROM python:3-9.slim
  WORKDIR /app
  COPY requirements.txt
  RUN pip install --nocache-dir -r requirements.txt
  COPY . .
  EXPOSE 5000
  CMD ["python","app.py"]
3. Now your dockerfile is created perfectly
4. Run dockerfile: docker run -d -p 5000:5000 python-docker-app
5. Now the container is launched & the code is running in that container
