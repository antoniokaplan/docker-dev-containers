# Quickstart - https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html
# Base Images - https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook
#  EXAMPLE - docker run -p 8888:8888 jupyter/scipy-notebook:2c80cf3537ca

# Base - jupyter/base-notebook

# + pandoc, git, TeX -
# jupyter/minimal-notebook

# + scikit, pandas, etc -
# Scipy - jupyter/scipy-notebook

# default pwd = /home/jovyan
FROM jupyter/base-notebook
ARG appdir=/usr/local
ARG npmg=$appdir/.npmglobal
# default user the container is started with
USER root
RUN mkdir -p $npmg && mkdir -p $npmg/bin
RUN chown -R jovyan $npmg

USER jovyan
WORKDIR  $appdir
RUN npm config set prefix $npmg
ENV PATH=$npmg/bin:$PATH
RUN npm install -g ijavascript

WORKDIR /home/jovyan/work
# RUN npm link ijavascript
RUN ijsinstall 

# switch to root and finish the javascript kernal installation
# USER root
