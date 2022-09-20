FROM pytorch/pytorch:1.6.0-cuda10.1-cudnn7-devel

RUN mkdir -p /workspace/data
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A4B469963BF863CC
RUN apt-get update
RUN apt-get install -y git && apt-get install -y neovim
RUN apt-get install -y wget && apt-get install -y curl && apt-get install unzip

RUN git clone https://github.com/PaulCCCCCCH/Multimodal-Categorization-of-Crisis-Events-in-Social-Media.git
RUN mv /workspace/Multimodal-Categorization-of-Crisis-Events-in-Social-Media /workspace/project
RUN cd ./project
RUN bash setup.py
RUN pip install tensorboard

RUN bash setup.sh
