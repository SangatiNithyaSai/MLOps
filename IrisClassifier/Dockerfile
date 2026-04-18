#using base Image
FROM python:3.12-slim
#creating a directory
WORKDIR /app
#copying and installing requirements at satrt so that when we rerun with changes
# the requirements are not re installed if there are no changes
COPY requirements.txt .

RUN python -m pip install --upgrade pip

RUN python -m pip install  -r requirements.txt
#now copy the .py files
COPY . .
#expose pose to use by users
EXPOSE 5001
#run the final command
CMD ["python","app.py"]
