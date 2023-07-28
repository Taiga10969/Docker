FROM nvidia/cuda:12.1.0-devel-ubuntu22.04

RUN apt-get update && apt-get upgrade -y --no-install-recommends && \
    apt-get install -y --no-install-recommends \
        vim \
        tmux \
        git \
        python3.10 \
        python3-pip \
        wget && \
    pip3 install --upgrade pip

COPY ./requirements.txt ./requirements.txt
RUN pip3 install -r ./requirements.txt

COPY ./start_jupyterlab.sh ./start_jupyterlab.sh
RUN chmod +x ./start_jupyterlab.sh
