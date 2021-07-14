FROM public.ecr.aws/j1r0q0g6/notebooks/notebook-servers/jupyter-pytorch-cuda-full:master-1831e436

USER root
# install - requirements.txt
RUN apt-get install -y libssl-dev libcurl4-openssl-dev python3-dev
COPY --chown=jovyan:users requirements.txt /tmp/requirements.txt
RUN python3 -m pip install -r /tmp/requirements.txt --no-cache-dir \
 && rm -f /tmp/requirements.txt

 USER ${NB_UID}