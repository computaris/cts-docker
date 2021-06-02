Prerequisites

Download:
1. TTS installer jar with name tts-installer*.jar

To build Docker image call `./build.sh`

Running:
- Mount license inside /usr/bin/TTS/bin
- Mount volume with test files
- Provide env variable JMX_PATH with path to jmx test file
