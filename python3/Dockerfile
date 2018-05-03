FROM debian:testing

RUN apt-get update && apt-get install -y \
  wget \
  git \
  make \
  python3 \
  python3-pip \
  # Removing documentation packages *after* installing them is kind of hacky,
  # but it only adds some overhead while building the image.
  apt-get --purge remove -y .\*-doc$ && \
  # Remove more unnecessary stuff
  apt-get clean -y

RUN pip3 install pytest pytest-cov pytest-mock
