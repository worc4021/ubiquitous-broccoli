# syntax=docker/dockerfile:1
FROM mcr.microsoft.com/devcontainers/cpp:1-debian-12

RUN apt update && \
    apt install -y ccache gfortran liblapack-dev \
    ca-certificates curl gnupg lsb-release libboost-all-dev \
    libhdf5-dev libcurl4-openssl-dev openscenegraph qtbase5-dev default-jre \
    uuid-dev flex


ADD https://github.com/OpenModelica/OpenModelica.git#v1.21.0 /openmodelica

WORKDIR /omcbuild

RUN cmake -B/omcbuild -H/openmodelica -DCMAKE_BUILD_TYPE=Release