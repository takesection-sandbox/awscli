Build
=====

```
export DOCKER_HOST=tcp://raspberrypi.local:2375
cd git
docker build . -t git
cd ../awscli
docker build . -t awscli
cd ..
```

# Usage

```
docker container create --name helper -v aws:/root busybox
docker cp ~/.aws/credentials helper:/root/
docker rm helper
```

```
docker run -it --rm -v aws:/root/.aws awscli ec2 describe-instances
```
