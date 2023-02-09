FROM nextflow/nextflow:${NF_DOCKER_TAG}
WORKDIR /
ENV INSTALLER="Miniconda3-py37_22.11.1-1-Linux-x86_64.sh"
ENV INSTALLER_URL="https://repo.anaconda.com/miniconda/${INSTALLER}"
RUN yum update -y && \
    yum install -y python3 wget && \
    wget ${INSTALLER_URL} && \
    bash ${INSTALLER} -b -p $HOME/miniconda && \
    conda config --add channels defaults && \
    conda config --add channels bioconda && \
    conda config --add channels conda-forge && \
    conda config --set channel_priority strict
ENV PATH=$HOME/miniconda/bin:$PATH
CMD ["bash"]
