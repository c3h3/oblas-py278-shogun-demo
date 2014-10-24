## Docker Images:

- [Base Image]: https://registry.hub.docker.com/u/c3h3/oblas-py278-shogun/
- [IPythonNotebbok]: https://registry.hub.docker.com/u/c3h3/oblas-py278-shogun-ipynb/

## How to use this images

```
docker run -p forward_port:8888 -v outside_ipynbs:/ipynbs -e IPYNB_PROFILE="c3h3-dark" -e OMP_NUM_THREADS=8 -d c3h3/oblas-py278-shogun-ipynb
```

- "forward_port" is the port you want to forward into docker image (EXPOSE 8888)
- "outside_ipynbs" is the directory you want to mount into docker image as /ipynbs  (WORKDIR)
- "IPYNB_PROFILE" is the environment variable could be set as "c3h3-dark" or "default"
- "OMP_NUM_THREADS" is the environment variable which would be read by openblas

