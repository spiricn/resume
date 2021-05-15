FROM ubuntu:20.04

ARG DEBIAN_FRONTEND=noninteractive
ENV DEBIAN_FRONTEND teletype

RUN apt update && apt -y install \
    texlive \
    lmodern \
    texlive-luatex \
    texlive-latex-extra

RUN luaotfload-tool --update

RUN apt-get update -y && apt-get install -y --no-install-recommends apt-utils
RUN echo ttf-mscorefonts-installer msttcorefonts/accepted-mscorefonts-eula select true | debconf-set-selections
RUN apt -y install ttf-mscorefonts-installer

