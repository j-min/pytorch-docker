FROM anibali/pytorch:cuda-9.0

# Install some basic utilities
RUN sudo apt-get update
RUN sudo apt-get install git -y
RUN sudo apt-get install build-essential -y
RUN sudo apt-get install expat libexpat1-dev -y

# Install ROUGE dependencies
RUN curl -L http://cpanmin.us | perl - --sudo App::cpanminus
RUN cpanm --sudo XML::DOM

RUN git clone https://github.com/falcondai/pyrouge
RUN cd pyrouge/RELEASE-1.5.5/data/WordNet-2.0-Exceptions && ./buildExeptionDB.pl . exc ../WordNet-2.0.exc.db
RUN cd pyrouge && python setup.py build && python setup.py install

RUN pip install pandas tqdm
RUN pip install nltk==3.4
