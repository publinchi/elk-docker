FROM sebp/elk

ADD ./cts-conf/02-beats-input.conf /etc/logstash/conf.d/02-beats-input.conf
ADD ./cts-conf/12-cts.conf /etc/logstash/conf.d/12-cts.conf

# Performance Tweaks
RUN echo "* - nofile 65535" >> /etc/security/limits.conf && \
    echo "* - memlock unlimited" >> /etc/security/limits.conf && \
    echo vm.max_map_count=262144 > /etc/sysctl.d/max_map_count.conf && \
    echo vm.swappiness=0 > /etc/sysctl.d/swappiness.conf

ENV ES_HEAP_SIZE 1g
ENV MAX_OPEN_FILES=65535
ENV MAX_LOCKED_MEMORY=unlimited
