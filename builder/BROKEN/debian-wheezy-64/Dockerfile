from debian:wheezy

RUN mv /etc/apt/sources.list /etc/apt/sources.list-orig;\
    awk '{print($0 " non-free");}' /etc/apt/sources.list-orig > /etc/apt/sources.list;\
    apt-get update; \
    apt-get install -y --force-yes \
                wget autoconf automake cvs gcc gfortran g++ valgrind libreadline-dev \
    	    	openjdk-7-jdk wget make rsync sudo pkg-config \
            	globus-common-progs libglobus-callout-dev \
		libglobus-gridmap-callout-error-dev \
		libglobus-gsi-credential-dev \
		libglobus-gsi-proxy-core-dev \
		libglobus-gss-assist-dev \
		libglobus-gssapi-gsi-dev \
		libglobus-xio-gsi-driver-dev  \
		freetds-dev libxml2-dev libcurl4-openssl-dev reprepro \
                libmotif-dev libxt-dev libxmu-dev libxp-dev libx11-dev \
                python-numpy python-nose; \
    apt-get -y upgrade;
RUN apt-get install -y --force-yes libdc1394-22-dev libraw1394-dev
RUN ln -s /usr/lib/libpython2.7.so.1.0 /usr/lib/libpython2.7.so
