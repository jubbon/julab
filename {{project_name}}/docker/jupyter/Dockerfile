ARG BASE_CONTAINER=jupyter/minimal-notebook:python-{{jupyter_python_version}}
FROM $BASE_CONTAINER

USER root

RUN apt-get update -y && apt-get upgrade -y

RUN python -m pip install --no-cache-dir --upgrade pip

COPY ./requirements.txt /opt/app/

RUN pip install --no-cache-dir -r /opt/app/requirements.txt

USER $NB_UID

WORKDIR /opt/app

ENV JUPYTER_ENABLE_LAB=1
