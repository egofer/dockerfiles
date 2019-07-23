FROM ubuntu:18.04
 
LABEL maintainer="emilio.gomez.fdez@gmail.com"
LABEL build_date="2019-07-12"

ENV LANG=es_ES.UTF-8
ENV PYTHONIOENCODING=utf-8

WORKDIR /home/

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update -y && apt upgrade -y && apt install python python-pip git qgis nano language-pack-es-base language-pack-ca-base language-pack-gl-base language-pack-eu-base -y

RUN git clone https://github.com/OSM-es/CatAtom2Osm.git

WORKDIR /home/CatAtom2Osm

# Add CatAtom2Osm requirements
RUN pip install -r requisites.txt
RUN make install
