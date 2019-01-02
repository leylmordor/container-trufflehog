# trufflehog [![Build Status](https://cloud.drone.io/api/badges/yellowmegaman/trfflhg/status.svg)](https://cloud.drone.io/yellowmegaman/trfflhg)

Alpine python image with trufflehog on board

##### Examples
```
docker run --rm -ti -v $PWD:/target yellowmegaman/trfflhg file:///target
```

```
docker run --rm -ti -v $PWD:/target yellowmegaman/trfflhg --regex --entropy=False https://github.com/dxa4481/truffleHog.git
```

###### Example for 1.x drone.io

```
kind: pipeline
name: github

steps:
- name: check for accidentally dropped creds
  image: yellowmegaman/trfflhg:2.0.98
  commands:
  - /usr/local/bin/trufflehog --regex --entropy=False file:///$CI_WORKSPACE
```
