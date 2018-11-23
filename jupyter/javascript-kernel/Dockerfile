FROM jupyter/base-notebook
ARG appdir=/usr/local
ARG npmg=$appdir/.npmglobal

# switch to root and create the folders & permissions
USER root
RUN mkdir -p $npmg && mkdir -p $npmg/bin
RUN chown -R jovyan $npmg

# switch back to default user and install javascript kernel
USER jovyan
WORKDIR  $appdir
RUN npm config set prefix $npmg
ENV PATH=$npmg/bin:$PATH
RUN npm install -g ijavascript

# the install
WORKDIR /home/jovyan/work
RUN ijsinstall
