FROM tchap/centos-epel

MAINTAINER Tomas Brambora "tomas@salsitasoft.com"

# Update packages
# RUN yum update -y --exclude=upstart

# Install Node.js
RUN yum install -y nodejs npm

RUN npm install -g grunt-cli
RUN npm install -g karma
Run npm install -g bower
Run npm install -g phantomjs

RUN yum install -y make
RUN yum install -y sudo
RUN yum install -y git
RUN yum install -y fontconfig

# Expose 3000
EXPOSE 3000

RUN useradd -m builder
#USER builder

# Run the thing
CMD ["make", "test"]
