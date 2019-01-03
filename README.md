# container-trufflehog [![Build Status](https://cloud.drone.io/api/badges/yellowmegaman/container-trufflehog/status.svg)](https://cloud.drone.io/yellowmegaman/container-trufflehog)

Alpine python image with trufflehog on board

##### Examples
```
docker run --rm -ti -v $PWD:/target yellowmegaman/container-trufflehog file:///target
```

```
docker run --rm -ti -v $PWD:/target yellowmegaman/container-trufflehog --regex --entropy=False https://github.com/dxa4481/truffleHog.git
```

###### Example for 1.x drone.io

```
kind: pipeline
name: github

steps:
- name: check for accidentally dropped creds
  image: yellowmegaman/container-trufflehog:2.0.98
  commands:
  - /usr/local/bin/trufflehog --regex --entropy=False file:///$CI_WORKSPACE
```
