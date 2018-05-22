FROM node:8-slim

RUN apt-get update && apt-get install -y unzip --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*
ADD https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-3.1.0.1141-linux.zip /opt
RUN unzip -q -d /opt/ /opt/sonar-scanner-cli-3.1.0.1141-linux.zip && \
    rm /opt/sonar-scanner-cli-3.1.0.1141-linux.zip
RUN mv /opt/sonar-scanner-3.1.0.1141-linux /opt/sonar-scanner

CMD ["/opt/sonar-scanner/bin/sonar-scanner"]
