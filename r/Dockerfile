FROM jupyter/r-notebook

# Installing CS-jupyterlab-grdm https://github.com/RCOSDP/CS-jupyterlab-grdm/
ENV grdm_jlab_release_tag=0.1.0 \
    grdm_jlab_release_url=https://github.com/RCOSDP/CS-jupyterlab-grdm/releases/download/0.1.0
RUN pip3 install ${grdm_jlab_release_url}/rdm_binderhub_jlabextension-refs.tags.${grdm_jlab_release_tag}.tar.gz \
    && jupyter labextension install ${grdm_jlab_release_url}/rdm-binderhub-jlabextension-refs.tags.${grdm_jlab_release_tag}.tgz \
    && jupyter labextension enable rdm-binderhub-jlabextension \
    && jupyter server extension enable rdm_binderhub_jlabextension \
    && jupyter nbextension install --py rdm_binderhub_jlabextension --user \
    && jupyter nbextension enable --py rdm_binderhub_jlabextension --user
