# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
FROM jupyter/base-notebook

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

USER root

# Install all OS dependencies for fully functional notebook server
RUN yum install -y \
    inkscape \
    jed \
    libsm6 \
    gcc \
    gcc-c++ \
    make \
    libxext-dev \
    libxrender1 \
    lmodern \
    netcat \
    python-dev \
    # ---- nbconvert dependencies ----
    texlive-xetex \
    texlive-fonts-recommended \
    texlive-plain-generic \
    # Optional dependency
    texlive-fonts-extra \
    # ----
    tzdata \
    unzip \
    nano && yum -y clean all

# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
