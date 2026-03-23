FROM docker.io/almalinux:10

RUN dnf update -y

RUN dnf install -y nss atk gtk3 libgfortran libXt

ADD matlab.tar.gz /opt/matlab

RUN mkdir -p /root/Documents/MATLAB

WORKDIR /root/Documents/MATLAB

CMD ["/opt/matlab/bin/matlab"," -nodisplay"]

