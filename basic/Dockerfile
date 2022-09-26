FROM pytorch/pytorch:1.6.0-cuda10.1-cudnn7-devel

RUN mkdir -p /workspace/data
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A4B469963BF863CC
RUN apt-get update
RUN apt-get install -y git && apt-get install -y neovim
RUN apt-get install -y wget && apt-get install -y curl && apt-get install -y unzip && apt-get install -y ufw

RUN apt-get install python3.9
RUN python3 -m pip install ipykernel -U --user --force-reinstall
RUN pip install jupyter notebook
RUN pip install tensorboard
RUN pip install matplotlib

RUN git config --global user.email omnyx2@gmail.com
RUN git config --global user.name omnyx2