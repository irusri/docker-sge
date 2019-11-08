docker-sge
==========

Dockerfile to build a container with SGE installed. Cloned and updated
from the docker-sge container from gawbul.

To build type:

```
git clone git@github.com:irusri/docker-sge.git
cd docker-sge
docker build -t irusri/docker-sge .
```

To pull from the Docker Hub type:

```
docker pull irusri/docker-sge
```

To run the image in a container type:

```
docker run -it --rm irusri/docker-sge login -f irusri
```

**You need the `login -f irusri` as root isn't allowed to submit jobs**

To submit a job run:

```
echo "echo Running test from $HOSTNAME" | qsub
```
