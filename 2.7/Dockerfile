FROM python:2.7

MAINTAINER Etienne Napoleone <etienne_napo@hotmail.com>

# install python and poetry
RUN curl -sSL https://raw.githubusercontent.com/sdispater/poetry/master/get-poetry.py | python

# create application directory
RUN mkdir /app
WORKDIR /app

# copy pyproject file
ONBUILD COPY pyproject.* .

# install dependencies:
ONBUILD RUN poetry install -n

# using this file
# ~~~~~~~~~~~~~~~
# FROM etiennenapoleone/poetry
# COPY . /app
# CMD python2 main.py
