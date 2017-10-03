FROM ubuntu:16.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y libssl-dev libjansson-dev libcurl4-openssl-dev libsqlite3-dev sendemail make gcc g++ git cmake
RUN mkdir /blackbird
WORKDIR /blackbird
RUN git clone --recursive  git://github.com/butor/blackbird.git .
RUN cmake -B./build -H. -DCMAKE_BUILD_TYPE=Release
RUN cmake --build ./build -- install

ENTRYPOINT ./blackbird
