FROM amd64/ubuntu:21.04
RUN apt update && apt upgrade -y
RUN apt-get install build-essential procps curl file git -y
RUN /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
ENV PATH="/home/linuxbrew/.linuxbrew/bin:${PATH}"
RUN brew install python && brew install python-tk@3.9 && brew install zip nasm libtool automake autoconf vim libarchive git-lfs
RUN apt install libcurl4-openssl-dev libarchive-tools zstd libpcre3-dev pacman libpcre3 libpcre3-dev -y
RUN mkdir /usr/devel && cd /usr/devel
RUN ssh-keygen -q -t rsa -N '' -f ~/.ssh/id_rsa
RUN ln -s /bin/gcc /bin/gcc-5

