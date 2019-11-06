FROM debian:stretch-slim

RUN apt-get update -y
RUN apt-get install -y wget gnupg pkg-config git python-pip flex bison gperf build-essential zip curl subversion libglib2.0-dev libgtk2.0-dev libxtst-dev libxss-dev libpci-dev libdbus-1-dev libgconf2-dev libgnome-keyring-dev libnss3-dev lsb-release sudo locales libssl-dev openssl cmake lbzip2

# depot tools
RUN git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
RUN echo 'export PATH=$PATH:/depot_tools' >> /root/.bashrc

COPY run.sh /
RUN chmod +x /run.sh

CMD /run.sh
