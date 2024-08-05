FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="Atom Developers <dev@atom.org>"
LABEL description="Dockerised Atom, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/atom

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} atom && \
    useradd -u ${USER_ID} -g atom -s /bin/bash -m -d /home/atom atom && \
    mkdir /home/atom/.atom && \
    chown ${USER_ID}:${GROUP_ID} -R /home/atom

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER atom

VOLUME ["/home/atom"]

EXPOSE 18761 9999 28761 28762

WORKDIR /home/atom
