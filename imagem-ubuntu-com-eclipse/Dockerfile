FROM ubuntu:14.10

RUN sudo apt-get update && apt-get install -y \
  wget \
  openjdk-7-jdk \
  libcanberra-gtk3-module && mkdir /eclipse 

RUN cd /eclipse && sudo wget --progress=bar:force \
  http://eclipse.c3sl.ufpr.br/technology/epp/downloads/release/mars/R/eclipse-jee-mars-R-linux-gtk-x86_64.tar.gz && \
  chmod +x eclipse-jee-mars-R-linux-gtk-x86_64.tar.gz && \
  tar -zxf eclipse-jee-mars-R-linux-gtk-x86_64.tar.gz

RUN cd /eclipse/eclipse/ && \
    sudo sed -i -e '1i-vm /usr/lib/jvm/java-7-openjdk-amd64/bin/java' eclipse.ini
