FROM sickcodes/docker-osx
RUN /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
CMD echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/arch/.profile
CMD eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
RUN brew install git python
RUN brew install python-tk@3.9 git-lfs nasm libarchive patchelf
ENV export PATH=/home/arch/.local/bin:$PATH
RUN ssh-keygen -q -t rsa -N '' -f ~/.ssh/id_rsa