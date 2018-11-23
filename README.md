# Docker containers for easy local development

## Jupyter notebooks

### Jupyter Javascript kernel
Base image with docker compose to mount local directory for notebook saving.
The image uses `jupyter/base-notebook` docker file and then adds `ijavascript` as the JS/Node Kernel

run using docker & mount `/notebooks` to save work:
```
  docker build -t jupyter-javascript .
  docker run --rm -d -v $(pwd)/notebooks:/home/jovyan/work -p 8888:8888 jupyter-javascript
```
or docker compose:
`docker-compose up --build`

Links to docs:
a. *Jupyter Quickstart* - [https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
b. *Base Images* - [https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook)
c. *ijavascript* - [https://github.com/n-riesco/ijavascript](https://github.com/n-riesco/ijavascript)
