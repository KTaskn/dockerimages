FROM python:3.9
LABEL maintainer="KTaskn"
LABEL github="https://github.com/KTaskn/dockerimages"

RUN pip install -U pip \
    && pip install numpy pandas scikit-learn matplotlib notebook
# docker build . --tag ktaskn/notebook

ENV workdir /home/jovyan
RUN mkdir $workdir
WORKDIR $workdir

CMD ["jupyter", "notebook", "--allow-root", "--port", "8888", "--ip", "0.0.0.0"]