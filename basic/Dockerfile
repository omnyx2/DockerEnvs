FROM pytorch/pytorch:1.6.0-cuda10.1-cudnn7-devel

RUN mkdir -p /workspace/data
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A4B469963BF863CC
RUN apt-get update
RUN apt-get install -y git && apt-get install -y neovim
RUN apt-get install wget && apt-get install curl

