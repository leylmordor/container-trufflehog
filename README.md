# trufflehog [![Build Status](https://cloud.drone.io/api/badges/yellowmegaman/trfflhg/status.svg)](https://cloud.drone.io/yellowmegaman/trfflhg)

Alpine python image with trufflehog on board

##### Example
```
docker run --rm -ti -v $PWD:/target yellowmegaman/trfflhg file:///target
```

```
docker run --rm -ti -v $PWD:/target yellowmegaman/trfflhg --regex --entropy=False https://github.com/dxa4481/truffleHog.git
```
