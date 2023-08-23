FROM debian:bookworm as base

ENV DEBIAN_FRONTEND=noninteractive

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
    python3-apt \
    python3-dev \
    python3-pip \
    python3-setuptools \
    python3-software-properties \
    python3-wheel \
    software-properties-common \
    sudo \
    wget \
 && rm -f /usr/lib/python3.11/EXTERNALLY-MANAGED \
 && python3 -m pip install --no-cache-dir -U pip wheel \
 && python3 -m pip install --no-cache-dir -U ansible \
 && rm -rf /var/lib/apt/lists/* /var/cache/apt/archives/*.deb \
 && apt-get autoremove \
 && apt-get clean

# Install Ansible inventory file.
RUN mkdir -p /etc/ansible \
 && echo "[local]\nlocalhost ansible_connection=local" > /etc/ansible/hosts

FROM base

# Initialize.
CMD ["/bin/bash"]