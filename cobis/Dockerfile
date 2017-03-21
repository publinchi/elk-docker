FROM sebp/elk

ADD ./cts-conf/02-beats-input.conf /etc/logstash/conf.d/02-beats-input.conf
ADD ./cts-conf/12-cts.conf /etc/logstash/conf.d/12-cts.conf

# Performance Tweaks
RUN sysctl -w vm.max_map_count=262144
