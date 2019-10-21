FROM ubuntu:18.04
WORKDIR /home

ENV ZIP_URL=https://github.com/kaischaabouni/TestDocker/files/3749708/archiveTest.zip
ENV ZIP_FILE=archiveTest.zip

RUN \
    apt-get update \
    && apt-get install -y software-properties-common \
    && apt-get install -y \
                        wget \
                        unzip \
    && rm -rf /var/lib/apt/lists/* 

RUN wget ${ZIP_URL} \
&& unzip ${ZIP_FILE} \
&& rm ${ZIP_FILE} 

COPY ./meta.xml /home/archiveTest/config/

#CMD cp /home/my_volume/config.xml /home/archiveTest/config/
