## Docker Images:

### - [Base Image](https://registry.hub.docker.com/u/c3h3/oblas-py278-shogun/)
### - [IPythonNotebbok](https://registry.hub.docker.com/u/c3h3/oblas-py278-shogun-ipynb/)

## How to use IPython Notebbok images

### Basic Usage:

```
docker run -p forward_port:8888 -v outside_ipynbs:/ipynbs -d c3h3/oblas-py278-shogun-ipynb
```
- "forward_port" is the port you want to forward into docker image (EXPOSE 8888)
- "outside_ipynbs" is the directory you want to mount into docker image as /ipynbs  (WORKDIR)



### Full Parameters Usage:
```
docker run -p forward_port:8888 -v outside_ipynbs:/ipynbs -e IPYNB_PROFILE="c3h3-dark" -e OMP_NUM_THREADS=8 -d c3h3/oblas-py278-shogun-ipynb
```

- "forward_port" is the port you want to forward into docker image (EXPOSE 8888)
- "outside_ipynbs" is the directory you want to mount into docker image as /ipynbs  (WORKDIR)
- "IPYNB_PROFILE" is the environment variable could be set as "c3h3-dark" or "default"
- "OMP_NUM_THREADS" is the environment variable which would be read by openblas



### [Go to Tutorial IPython Notebook !!!](http://nbviewer.ipython.org/github/c3h3/oblas-py278-shogun-demo/blob/master/demo_ipynbs/Step1_docker_pull_and_run.ipynb)

### [Go to Demo Repository !!!](https://github.com/c3h3/oblas-py278-shogun-demo)


