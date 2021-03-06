# Jupyter Docker stacks based on Centos 7

Instead of Ubuntu, using centos 7,
made minimal changes, mostly apt -> yum

Don't have autobuild yet, currently just pushing to: <https://hub.docker.com/repository/docker/zonca/jupyter-docker-stacks-centos7>

I am interested in the `tensorflow` image so I have built it and pushed it to DockerHub with the `tensorflow` tag.

In the future possibly setup autobuild to build all the requirements, i.e. `base-notebook`, `minimal-notebook`, `scipy-notebook`.

How to build the images:

```
make build/base-notebook
make build/minimal-notebook
make build/scipy-notebook
make build/tensorflow-notebook
```

or

```
make build-all
```

Make sure the machine has `pass`

```
sudo apt install pass
```

Then:

```
docker login
export VERSION=2020.07
docker tag zonca/jupyter-docker-stacks-centos7  zonca/jupyter-docker-stacks-centos7:tensorflow-$VERSION
docker push zonca/jupyter-docker-stacks-centos7:tensorflow-$VERSION
```
