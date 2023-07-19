FROM pytorch/pytorch:1.10.0-cuda11.3-cudnn8-devel

ENV UID 12345
ENV USER_NAME user
ENV CUDA cu113
ENV TORCH 1.10.0

# install essential softwares
RUN apt update && apt install -y vim zsh git ssh sudo language-pack-en tmux
RUN update-locale LANG=en_US.UTF-8

# link to python
RUN ln -s /opt/conda/bin/python /usr/bin/python

# python -m pip install packages
RUN python -m pip install --upgrade pip
RUN python -m pip install numpy matplotlib pylint tqdm sentencepiece transformers scikit-learn tensorboard spacy==2.3.7 scispacy black seaborn

# install optuna
RUN apt install -y libssl-dev python3-dev libmysqlclient-dev sqlite3 && python -m pip install optuna mysqlclient scikit-optimize

# install scispaCy
RUN python -m pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.2.5/en_core_sci_sm-0.2.5.tar.gz

# install deep graph library
RUN python -m pip install dgl-cu113 -f https://data.dgl.ai/wheels/repo.html
RUN python -m pip install outdated ogb

RUN adduser --uid ${UID} --force-badname --shell /bin/zsh --disabled-password --no-create-home ${USER_NAME} \
    && echo ${USER_NAME}:${USER_NAME} | chpasswd \
    && ln -s /workspace /home/${USER_NAME} \
    && chown ${USER_NAME}:${USER_NAME} /workspace && chmod 755 /workspace
RUN git clone https://github.com/iryuki1110/my_setting.git /root/my_setting && cp /root/my_setting/.zshrc /home/${USER_NAME}/.zshrc && chown ${USER_NAME}:${USER_NAME} /home/${USER_NAME}/.zshrc

USER ${USER_NAME}
CMD ["/usr/bin/zsh"]
