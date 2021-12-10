FROM debian:bullseye
WORKDIR /app

RUN apt-get update
RUN apt-get install -y openssh-client wget tree curl screen git
RUN apt-get install -y postgresql-client

# Install corkscrew
# https://github.com/bryanpkc/corkscrew
RUN git clone https://github.com/bryanpkc/corkscrew.git
WORKDIR /app/corkscrew
RUN apt-get install -y build-essential autoconf
RUN autoreconf --install
RUN ./configure
RUN make
RUN make install
