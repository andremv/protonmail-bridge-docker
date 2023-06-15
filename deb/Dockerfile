FROM debian:bookworm
# LABEL maintainer="Xiaonan Shen <s@sxn.dev>"
LABEL maintainer="Andrei Moldovan <dev@andrei.me.uk>"

EXPOSE 25/tcp
EXPOSE 143/tcp

WORKDIR /protonmail

# Copy bash scripts
COPY gpgparams install.sh entrypoint.sh VERSION /protonmail/

# Install dependencies and protonmail bridge
RUN bash install.sh

ENTRYPOINT ["bash", "/protonmail/entrypoint.sh"]
