FROM ktaskn/notebook
LABEL maintainer="KTaskn"
LABEL github="https://github.com/KTaskn/dockerimages"

USER root

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y tzdata libopencv-dev libgl1-mesa-dev

USER jovyan

RUN pip install -U pip \
    && pip install opencv-python

CMD [".local/bin/jupyter", "notebook", "--allow-root", "--port", "8888", "--ip", "0.0.0.0"]