# Jupyter Docker stacks based on Centos 7

Instead of Ubuntu, using centos 7,
made minimal changes, mostly apt -> yum

Don't have autobuild yet, currently just pushing to: <https://hub.docker.com/repository/docker/zonca/jupyter-docker-stacks-centos7>

I am interested in the `tensorflow` image so I have built it and pushed it to DockerHub with the `tensorflow` tag.

In the future possibly setup autobuild to build all the requirements, i.e. `base-notebook`, `minimal-notebook`, `scipy-notebook`.
