FROM openjdk:8 as builder

COPY data/auto-install.xml /tmp
COPY tts-installer*.jar /tmp

RUN java -jar /tmp/tts-installer*.jar /tmp/auto-install.xml

FROM openjdk:8

COPY --from=builder /usr/bin/TTS /usr/bin/TTS

RUN chmod +x /usr/bin/TTS/bin/jmeter.sh
RUN chmod +x /usr/bin/TTS/bin/jmeter

WORKDIR /usr/bin/TTS/bin

ENTRYPOINT ["bash", "-c", "./jmeter.sh -n -t $JMX_PATH"]
