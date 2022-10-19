# DockerFile to build basic Oracle Linux container image
# Based on Oracle Linux 9

# Set the base image to Oracle Linux 8
FROM oraclelinux:8

# File Author / Maintainer
LABEL maintainer="anthony-marais"

# Update the repository sources list
RUN yum -y update && yum clean all
# Upgrade the installed packages
RUN yum -y upgrade && yum clean all

RUN yum -y install wget && yum clean all
RUN yum -y install openssl && yum clean all


RUN wget https://download.oracle.com/otn-pub/otn_software/db-express/oracle-database-xe-21c-1.0-1.ol8.x86_64.rpm?AuthParam=1666186460_132b0c3c65cbd26cee261704f5ab9616


#RUN wget https://download.oracle.com/otn-pub/otn_software/db-express/oracle-database-xe-21c-1.0-1.ol8.x86_64.rpm
#RUN curl -o oracle-database-preinstall-21c-1.0-1.el8.x86_64.rpm https://yum.oracle.com/repo/OracleLinux/OL8/appstream/x86_64/getPackage/oracle-database-preinstall-21c-1.0-1.el8.x86_64.rpm
#RUN yum -y localinstall oracle-database-preinstall-21c-1.0-1.el8.x86_64.rpm
#RUN rm oracle-database-preinstall-21c-1.0-1.el8.x86_64.rpm
#RUN yum install -y oracle-database-preinstall-21c

# RUN yum -y localinstall oracle-database-xe*

#RUN /etc/init.d/oracle-xe-21c configure


# Set the default command to run on boot
# This will boot Oracle Database in a DBCA created XE database
CMD ["/bin/bash"]

# Expose the default port for Oracle Database
#EXPOSE 1521

# Set the default environment variables for the Oracle Database installation
#ENV ORACLE_BASE=/opt/oracle \
#    ORACLE_HOME=/opt/oracle/product/19c/dbhomeXE \
#    ORACLE_SID=XE \
#    ORACLE_PWD=oracle \
#    INSTALL_DIR=/opt/install \
#    PATH=/usr/sbin:$PATH \
#    PATH=$ORACLE_HOME/bin:$PATH \
#    LD_LIBRARY_PATH=$ORACLE_HOME/lib:/lib:/usr/lib \
#    CLASSPATH=$ORACLE_HOME/jlib:$ORACLE_HOME/rdbms/jlib

## Create the installation directory
#RUN mkdir -p $INSTALL_DIR

# Copy the installation files

#COPY oracle-database-xe-19c-1.0-1.x86_64.rpm $INSTALL_DIR

# Install Oracle Database XE
#RUN yum -y localinstall $INSTALL_DIR/oracle-database-xe-19c-1.0-1.x86_64.rpm && \
#    rm -rf $INSTALL_DIR && \
#    yum clean all

# Define default command to start Oracle Database.
#CMD exec $ORACLE_BASE/$START_FILE

# Expose ports
#EXPOSE 1521 5500

# Define default command to start Oracle Database.
#CMD exec $ORACLE_BASE/$START_FILE

# END OF FILE