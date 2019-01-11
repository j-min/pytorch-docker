FROM pytorch/pytorch:1.0-cuda10.0-cudnn7-runtime

RUN apt-get update

RUN apt-get install build-essential -y

RUN curl -L https://cpanmin.us | perl - App::cpanminus

RUN apt-get install expat -y
RUN apt-get install libexpat1-dev -y

RUN cpanm XML::DOM

RUN conda install pandas tqdm \
 && conda clean -ya

RUN pip install nltk==3.4
