# Jupyter notebook basics
EXAMPLE -
`docker run -p 8888:8888 jupyter/scipy-notebook:2c80cf3537ca`

Links to docs:
a. *Jupyter Quickstart* - [https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
b. *Base Images* - [https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook)
c. *ijavascript* - [https://github.com/n-riesco/ijavascript](https://github.com/n-riesco/ijavascript)


## Jupyter Notebook images

### Base
jupyter/base-notebook

### minimal
+ pandoc, git, TeX -
jupyter/minimal-notebook

### scipy
+ scikit, pandas, etc -
jupyter/scipy-notebook

## Notes on Docker Jupyter environment
a. notebooks run with default user `jovyan`
b. default pwd = /home/jovyan/work
