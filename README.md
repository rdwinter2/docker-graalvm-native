# Docker + GraalVM native-image

0. Download Oracle GraalVM Enterprise Edition Native Image preview for Linux (19.2.1) from [Downloads/Oracle GraalVM Enterprise Edition](https://www.oracle.com/downloads/graalvm-downloads.html).
1. create locally the `graalvm-native-image` container using `graalvm-native-image/build.sh`. This container will be used to build the native image.
2. run sbt
3. run in sbt: `dockerGraalvmNative`: this will generate the `docker-graalvm-native-test` container
4. run in sbt: `docker:publishLocal`: this will generate the `docker-test` continer
5. run in shell: `time docker run --rm docker-graalvm-native-test`
6. run in shell: `time docker run --rm docker-test` and compare the timing
7. run `docker images | grep docker-` and compare the image size