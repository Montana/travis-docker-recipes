
# Travis Docker Recipes

By default, the image is built using the same architecture as the host/build machine. To override that, pass a valid platform string:
```sh
# build for arm64
$ docker build -t harmony --platform linux/arm64 .

# build for amd64
$ docker build -t harmony --platform linux/amd64 .
```

## Override Version of Go
The default version is set to `1.16.3`. To override this with another `1.16.x` distro, pass `--build-arg GOLANG_VERSION=x.x.x`. Example:
```sh
$ docker build --build-arg GOLANG_VERSION=1.16.13 -t harmony .
```
