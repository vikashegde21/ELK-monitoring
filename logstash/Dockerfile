FROM docker.elastic.co/logstash/logstash:8.11.0

# Remove default pipeline
RUN rm -f /usr/share/logstash/pipeline/logstash.conf

# Add custom pipeline
COPY pipeline/ /usr/share/logstash/pipeline/

# Install additional plugins if needed
RUN logstash-plugin install logstash-input-beats