[![Build Status](https://travis-ci.com/slauger/openshift-toolbox.svg?branch=master)](https://travis-ci.com/slauger/openshift-toolbox)

# openshift-toolbox

OpenShift Toolbox and Install Images for OKD4 and OCP4.

## Run

### Docker

```
docker run -it quay.io/slauger/openshift-toolbox:<openshift-version>
```

### Podman

```
podman run -it quay.io/slauger/openshift-toolbox:<openshift-version>
```

## Build OCP

```
export DEPLOYMENT_TYPE=ocp
export RELEASE_CHANNEL=stable-4.7
export OPENSHIFT_RELEASE=$(make print_version)
export CONTAINER_NAME=registry.local/openshift-toolbox
```

## Build OKD

```
export DEPLOYMENT_TYPE=okd
export OPENSHIFT_RELEASE=$(make print_version)
export CONTAINER_NAME=registry.local/openshift-toolbox
```

## Run Build

```
make fetch
make build
make test
make push
```

