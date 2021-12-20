# Setup workspace with juypyterlab + code-server

My workspace setup to using nvidia/cuda as root container for code-server and jupyterlab.

## Docker-compose

### Sub domain

- `docker-compose -f docker-compose.subdomain.yml --env-file .subdomain.env up`

- [code.localhost](code.localhost): code-server
- [jupyterlab.localhost](jupyterlab.localhost): jupyterlab

### Sub path

- `docker-compose -f docker-compose.subpath.yml --env-file .subpath.env up`

- [localhost/workspace/code](code.localhost): code-server
- [localhost/workspace/jupyterlab](jupyterlab.localhost): jupyterlab

## Cuda as root container

- Change image to gpu-version.
- un-comment: `runtime: nvidia`, `NVIDIA_VISIBLE_DEVICES: all`, `NVIDIA_DRIVER_CAPABILITIES: all`

### Password

- run `python gen_pass.py` to get password (default pass: password)

## Acknowledgements

- [github.com/jupyter/docker-stacks](https://github.com/jupyter/docker-stacks)
- [github.com/cdr/code-server](https://github.com/cdr/code-server)
