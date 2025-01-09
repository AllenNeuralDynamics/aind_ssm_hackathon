# hash:sha256:b669600cec5cf8f3509e87cc31f1ddfbbfbe81919d8e1b403ce13d4ff9262413
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.6.1-miniconda4.12.0-python3.9-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

ENV PYTHONPATH="${PYTHONPATH}:/root/capsule/code"

RUN pip install -U --no-cache-dir \
    allensdk==2.16.2 \
    dynamax[notebooks]==0.1.5 \
    ipywidgets==8.1.5 \
    jax[cpu]==0.4.23 \
    numpy==1.23.4 \
    scikit-learn==1.3.0
