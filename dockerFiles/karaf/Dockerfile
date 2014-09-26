FROM dockerfile/java
MAINTAINER brandon grantham <bgrantham@gmail.com>

RUN wget http://apache.openmirror.de/karaf/3.0.1/apache-karaf-3.0.1.tar.gz; \
    mkdir /opt/karaf; \
    tar --strip-components=1 -C /opt/karaf -xzvf apache-karaf-3.0.1.tar.gz; \
    rm apache-karaf-3.0.1.tar.gz; \
    mkdir /deploy; \
    sed -i 's/^\(felix\.fileinstall\.dir\s*=\s*\).*$/\1\/deploy/' /opt/karaf/etc/org.apache.felix.fileinstall-deploy.cfg

ENTRYPOINT ["/opt/karaf/bin/karaf"]
