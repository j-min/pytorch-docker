FROM anibali/pytorch:cuda-9.0

RUN sudo apt-get update

RUN sudo apt-get install build-essential -y

RUN curl -L https://cpanmin.us | perl - --sudo App::cpanminus

RUN sudo apt-get install expat -y
RUN sudo apt-get install libexpat1-dev -y

RUN sudo cpanm XML::DOM

RUN conda install pandas tqdm \
 && conda clean -ya

RUN pip install nltk==3.4
