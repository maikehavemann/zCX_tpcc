FROM s390x/ibmjava:jre
RUN mkdir /opt/shareclasses
RUN mkdir /home/oltpbench
WORKDIR /home/oltpbench
COPY ./oltpbench .
CMD ["./oltpbenchmark", "-b", "tpcc", "-c", "config/db2_tpcc_config.xml", "--create=false", "--load=false", "--execute=true", "-s", "5", "-o", "outputfile", "--histograms"]