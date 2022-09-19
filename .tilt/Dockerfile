FROM python
RUN pip install bzt
RUN apt-get update && apt-get -y install default-jre-headless
RUN bzt -install-tools -o modules.install-checker.include=jmeter
COPY test.yml test.yml
WORKDIR /tmp
ENTRYPOINT ["bzt"]