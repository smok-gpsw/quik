# quik in ubuntu
How to build quik Engine in linux:
* Run docker build `docker build --build-arg SSH_KEY="$(cat ~/.ssh/id_rsa)" -t {docker_name} .`
* Run container with bash `docker run -it {docker_name} /bin/bash`
* Set SSH key in github with public key from ~/.ssh/id_rsa.pub and make authorize SSO for gopro/GPFW.
* Get to devel folder `cd /usr/devel` and install sx `pip3 install --user --upgrade "git+ssh://git@github.com/gopro/gopro-util-sx-bundle.git#egg=bundle"`
* Add sx to PATH `export PATH=/root/.local/bin:$PATH`
* Install bundle `sx init git@github.com:gopro/gopro-quik-bundle-conf.git`
* Subscribe to quik engine `sx topic --subscribe quik-engine`
* Build quik `sx update` after build success you can test them by running below command to generate mp4 file
`source sx/activate.sh` and `crafter render ./stupeflix_crafter/craftests/craftests/tests/themes/test_regression_all_themes.py adrenaline_complete_large -o test.mp4`
  It will generate test.mp4 file if the test works.
  
More information on set up quik engine https://wiki-dev.gopro.com/pages/viewpage.action?pageId=171024727

# quik in Mac
How to build quik Engine in linux:
* Run docker build `docker build --build-arg SSH_KEY="$(cat ~/.ssh/id_rsa)" -t {docker_name} .`
* Run container with bash `docker run -it {docker_name} /bin/bash`
* Set SSH key in github with public key from ~/.ssh/id_rsa.pub and make authorize SSO for gopro/GPFW.
* Get to devel folder `cd /usr/devel` and install sx `pip3 install --user --upgrade "git+ssh://git@github.com/gopro/gopro-util-sx-bundle.git#egg=bundle"`
* Add sx to PATH `export PATH=/home/arch/.local/bin:$PATH`
* Install bundle `sx init git@github.com:gopro/gopro-quik-bundle-conf.git`
* Subscribe to quik engine `sx topic --subscribe quik-engine`
* Build quik `sx update` after build success you can test them by running below command to generate mp4 file
  `source sx/activate.sh` and `crafter render ./stupeflix_crafter/craftests/craftests/tests/themes/test_regression_all_themes.py adrenaline_complete_large -o test.mp4`
  It will generate test.mp4 file if the test works.

