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

RUN git clone https://github.com/omnyx2/Multimodal-Categorization-of-Crisis-Events-in-Social-Media-1.git
RUN mv /workspace/Multimodal-Categorization-of-Crisis-Events-in-Social-Media /workspace/project
RUN ls && cd project && mkdir datasets && ls && cd ./datasets && \
    wget https://crisisnlp.qcri.org/data/crisismmd/CrisisMMD_v2.0.tar.gz && \ 
    tar -zxf CrisisMMD_v2.0.tar.gz && \
    cd CrisisMMD_v2.0 && \ 
    unzip crisismmd_datasplit_all.zip && \
    rm crisismmd_datasplit_all.zip && \
    cd .. && \
    rm CrisisMMD_v2.0.tar.gz && \
    cd ..


RUN pip install imageio==2.9.0
RUN pip install nltk==3.6.3
RUN pip install numpy==1.20.3
RUN pip install Pillow==8.4.0
RUN pip install scikit_learn==1.0.1
RUN pip install termcolor==1.1.0

# RUN pip install torch==1.9.0
# RUN pip install torchvision==0.10.0
RUN pip install tqdm==4.62.2
RUN pip install transformers==4.11.0

# RUN bash setup.py
