FROM pytorch/pytorch:2.0.1-cuda11.7-cudnn8-devel
RUN pip install jupyterlab notebook voila
RUN  apt-get update && DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt-get -y install tzdata && apt-get install ffmpeg libsm6 libxext6  -y
RUN pip install pandas matplotlib tensorboard nltk