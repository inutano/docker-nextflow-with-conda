FROM nextflow/nextflow:22.10.6
WORKDIR /
ENV INSTALLER="Miniconda3-py37_22.11.1-1-Linux-x86_64.sh"
ENV INSTALLER_URL="https://repo.anaconda.com/miniconda/${INSTALLER}"
ENV PATH="/miniconda/bin:$PATH"
RUN yum update -y && \
    yum install -y python3 wget && \
    wget ${INSTALLER_URL} && \
    bash ${INSTALLER} -b -p /miniconda && \
    conda config --add channels defaults && \
    conda config --add channels bioconda && \
    conda config --add channels conda-forge && \
    conda config --set channel_priority strict
CMD ["bash"]
