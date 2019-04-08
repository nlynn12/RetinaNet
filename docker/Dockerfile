FROM pytorch/pytorch:1.0.1-cuda10.0-cudnn7-runtime

RUN apt-get update && apt-get install -y --no-install-recommends \
         apt-utils \
         build-essential \
         cmake \
         git \
         curl \
         nano \
         python3-dev \ 
         python3-pip \
         python3-setuptools \
         net-tools \
         iputils-ping \
         ca-certificates &&\
     rm -rf /var/lib/apt/lists/*

RUN pip3 install --upgrade pip

RUN pip3 uninstall -y pillow
RUN pip3 install pillow-simd

RUN pip3 install torchvision

RUN pip3 install Cython
RUN pip3 install pycocotools

#RUN echo 'alias python="/usr/bin/python3"' >> ~/.bashrc
