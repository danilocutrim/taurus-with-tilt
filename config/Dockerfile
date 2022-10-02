FROM python
RUN pip install bzt
RUN apt-get update && apt-get -y install default-jre-headless
RUN apt-get -y install nano
RUN bzt -install-tools -o modules.install-checker.include=jmeter
ADD .bzt-rc /temp/.bzt-rc
ADD test.yml /bzt-configs/test.yml
ADD *.jmx /bzt-configs
ADD *.jar /bzt-configs
WORKDIR /bzt-configs
ENTRYPOINT ["bzt"]