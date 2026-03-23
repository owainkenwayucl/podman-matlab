FROM docker.io/almalinux:10

RUN dnf update -y

RUN dnf install -y nss atk gtk3 libgfortran libXt wget

RUN wget https://www.mathworks.com/mpm/glnxa64/mpm -O /root/mpm

RUN chmod 700  /root/mpm

RUN /root/mpm install --release=R2025b --destination=/opt/matlab --products=MATLAB Parallel_Computing_Toolbox

RUN mkdir -p /opt/matlab/licenses

ADD network.lic /opt/matlab/licenses/network.lic

RUN mkdir -p /root/Documents/MATLAB

WORKDIR /root/Documents/MATLAB

CMD ["/opt/matlab/bin/matlab"," -nodisplay"]

