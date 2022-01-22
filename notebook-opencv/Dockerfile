FROM ktaskn/notebook
LABEL maintainer="KTaskn"
LABEL github="https://github.com/KTaskn/dockerimages"

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y tzdata libopencv-dev libgl1-mesa-dev
    
RUN pip install -U pip \
    && pip install opencv-python

CMD ["jupyter", "notebook", "--allow-root", "--port", "8888", "--ip", "0.0.0.0"]