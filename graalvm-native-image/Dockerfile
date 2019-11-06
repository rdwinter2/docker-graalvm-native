FROM oracle/graalvm-ce:19.2.1
WORKDIR /opt/graalvm
COPY native-image-installable-svm-svmee-linux-amd64-19.2.1.jar /tmp/native-image.jar
RUN gu --local-file install /tmp/native-image.jar
ENTRYPOINT ["native-image"]