FROM python
RUN pip install bzt
RUN apt-get update && apt-get -y install default-jre-headless
RUN bzt -install-tools -o modules.install-checker.include=jmeter
ADD .bzt-rc /temp/.bzt-rc
ADD test.yml /tmp/test.yml
WORKDIR /tmp
ENTRYPOINT ["bzt test.yml"]