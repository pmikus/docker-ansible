FROM ubuntu:20.04 as base

ENV DEBIAN_FRONTEND=non-interactive

# Install required dependencies.
RUN apt-get update -y \
 && apt-get --no-install-recommends -y upgrade \
 && apt-get install --no-install-recommends -y \
    apt-transport-https \
    curl \
    gcc \
    gnupg \
    iputils-ping \
    iproute2 \
    python3 \
    python3-dev \
    python3-pip \
    python3-setuptools \
    python3-software-properties \
    software-properties-common \
    sudo \
    wget \
 && python3 -m pip install --no-cache-dir -U pip wheel \
 && python3 -m pip install --no-cache-dir -U ansible \
 && rm -rf /var/lib/apt/lists/* /var/cache/apt/archives/*.deb \
 && apt-get autoremove \
 && apt-get clean

FROM base

# Initialize.
CMD ["/bin/bash"]