FROM sickcodes/docker-osx
RUN /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
ENV PATH="/home/linuxbrew/.linuxbrew/bin:${PATH}"
RUN brew install git python python-tk@3.9 git-lfs nasm libarchive patchelf
ENV export PATH=/home/arch/.local/bin:$PATH
RUN ssh-keygen -q -t rsa -N '' -f ~/.ssh/id_rsa