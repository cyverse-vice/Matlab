FROM FROM mathworks/matlab:r2021a

# Install a few dependencies for iCommands, text editing, and monitoring instances
RUN apt-get update && apt-get install -y lsb-release wget apt-transport-https curl supervisor nginx gnupg2 libfuse2 nano htop gcc less nodejs software-properties-common apt-utils glances

RUN wget -qO - https://packages.irods.org/irods-signing-key.asc | apt-key add - && \
    echo "deb [arch=amd64] https://packages.irods.org/apt/ bionic main" > /etc/apt/sources.list.d/renci-irods.list && \
    apt-get update && \
    wget -c \
    http://security.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_1.22-1ubuntu0.18.04.2_all.deb \
    http://security.ubuntu.com/ubuntu/pool/main/r/requests/python-requests_2.18.4-2ubuntu0.1_all.deb \
    http://security.ubuntu.com/ubuntu/pool/main/o/openssl1.0/libssl1.0.0_1.0.2n-1ubuntu5.6_amd64.deb && \
    apt install -y \
    ./python-urllib3_1.22-1ubuntu0.18.04.2_all.deb \
    ./python-requests_2.18.4-2ubuntu0.1_all.deb \
    ./libssl1.0.0_1.0.2n-1ubuntu5.6_amd64.deb && \
    rm -rf \
    ./python-urllib3_1.22-1ubuntu0.18.04.2_all.deb \
    ./python-requests_2.18.4-2ubuntu0.1_all.deb \
    ./libssl1.0.0_1.0.2n-1ubuntu5.6_amd64.deb

RUN apt install -y irods-icommands

ENTRYPOINT ["/bin/run.sh"]

CMD ["-vnc"]
