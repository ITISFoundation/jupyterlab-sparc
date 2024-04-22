# JupyterLab with SPARC Tools

JupyterLab with Python kernel and different SPARC-relevand tools installed, including the [SPARC Python Client](https://docs.sparc.science/docs/sparc-python-client) and Python dependencies from [Docker_SPARC](https://github.com/cchorn/Docker_SPARC).

## How to develop this o²S²PARC Service

This Service was build using the [o²S²PARC cookiecutter for JupyterLab services](https://github.com/ITISFoundation/cookiecutter-osparc-jupyterlab-service)
### Usage

Build the module:
```console
$ make build
```
To run locally at and visit http://127.0.0.1:8888
```console
make run-local
```
To publish in local throw-away registry:
```console
make publish-local
```


### Versioning
Service version is updated with ``make version-*``

### CI/CD Integration 
A template ci config file is created in ```.github/workflows/check-image.yml```, it checks that the image builds. When the workflow runs successfully for a new version (on the main branch), this is automatically detected and published on the internal registry (see also "Deployment on o²S²PARC" in this README)

### Deployment on o²S²PARC

The required CI is already packaged.
To build and push to the internal registry you must add it to the [oSparc/docker-publisher-osparc-services](https://git.speag.com/oSparc/docker-publisher-osparc-services) repository.

## How to test the Application
Run locally and visit http://127.0.0.1:8888:
```console
make run-local
```
Or publish it in a local o²S²PARC deploy:
```console
make publish-local
```
Execute the code snippets of one the SPARC Python Client Tutorial, for example [Download public data, scaffolds and run computations](https://docs.sparc.science/docs/getting-started-with-the-sparc-python-client)

## Changelog

### [1.0.3] - 2024-04-22
Final version (for production)

### [1.0.0] - 2024-04-18
First version

