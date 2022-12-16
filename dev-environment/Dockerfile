FROM python:3.10-slim

# set the working directory
WORKDIR /workspaces/python-docker-devcontainer

# install dependencies
COPY ./requirements.txt ./
RUN pip install --disable-pip-version-check --no-cache-dir --upgrade -r requirements.txt

# copy the src to the folder
COPY ./src ./src

# start the server
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "80", "--reload"]
