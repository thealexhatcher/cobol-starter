FROM alpine:latest
RUN apk update \
    && apk upgrade \
    && apk add --no-cache sudo wget git openssh
RUN adduser -D vscode && mkdir -p /etc/sudoers.d \
    && echo "vscode ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode
USER vscode
WORKDIR $HOME

RUN sudo apk add --update --no-cache \
    file \
    gdb \
    gmp \
    gmp-dev \
    libltdl \
    ncurses \
    ncurses-dev \
    db-dev \
    gcc \
    libgcc \
    libc-dev \
    gettext-dev \
    libxml2-dev \
    make

#RUN cd /tmp \
#    wget http://sourceforge.net/projects/gnucobol/files/gnu-cobol/3.1/gnucobol-3.1.2.tar.gz \
#    && tar xvf gnucobol-3.1.2.tar.gz \
#    && cd gnucobol-3.1.2 \
#    && ./configure \
#    && make \
#    && make check \
#    && sudo make install \
#    && sudo ldconfig
