# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
ARG BASE_CONTAINER=jupyter/scipy-notebook
FROM $BASE_CONTAINER

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Install Tensorflow
RUN pip install --quiet --no-cache-dir \
    'tensorflow==2.4.1' && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

# Install autokeras
RUN pip install autokeras

# Install auto-skleran
RUN sudo apt-get update
RUN sudo apt-get install build-essential swig
RUN pip3 install auto-sklearn

# Install additional python packages
RUN pip3 install graphviz
RUN pip3 install pandas-profiling
RUN pip3 install PipelineProfiler
RUN pip3 install pickle
RUN pip install icd10-cm
RUN pip3 install graphviz
RUN pip3 install seaborn
RUN pip3 install spacy
RUN pip3 install gensim
RUN pip3 install pyLDAvis
