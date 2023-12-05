FROM docker.io/jupyter/scipy-notebook:python-3.11.6

USER root

### System dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        lmodern \
        file \
        curl \
        tmux && \
    apt-get clean -y && \
    rm -rf /var/lib/apt/lists/* /tmp/library-scripts

### R compiler settings


### Quarto
# versions: https://quarto.org/docs/download/_download.json
# neat setup: https://github.com/jeremiahpslewis/reproducibility-with-quarto


USER ${NB_USER}

### R development




### Prints Jupyter server token when terminal is opened
RUN echo "echo \"Jupyter server token: \$(jupyter server list 2>&1 | grep -oP '(?<=token=)[[:alnum:]]*')\"" > ${HOME}/.get-jupyter-url.sh && \
    echo "sh \${HOME}/.get-jupyter-url.sh" >> ${HOME}/.bashrc
