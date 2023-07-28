FROM nvidia/cuda:11.4.0-devel-ubuntu20.04

RUN apt-get update && apt-get upgrade -y --no-install-recommends
RUN apt-get install -y --no-install-recommends \
    vim \
    tmux \
    git \
    python3 \
    python3-pip \
    wget \

RUN pip3 install --upgrade pip
COPY ./requirements.txt ./requirements.txt
RUN pip3 install -r ./requirements.txt
COPY ./start_jupyterlab.sh ./start_jupyterlab.sh
RUN chmod +x ./start_jupyterlab.sh
