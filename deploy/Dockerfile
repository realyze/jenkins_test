FROM tchap/centos-epel

MAINTAINER Tomas Brambora "tomas@salsitasoft.com"

# Update packages
# RUN yum update -y --exclude=upstart

# Install Node.js
RUN yum install -y nodejs npm

RUN npm install -g mocha

RUN yum install -y make
RUN yum install -y sudo
RUN yum install -y git
RUN yum install -y fontconfig

# Install Supervisord
RUN yum install -y python-setuptools
RUN easy_install supervisor

# Expose 3000
EXPOSE 3000

RUN useradd -m builder
#USER builder

# Run the thing
CMD ["make", "test"]
