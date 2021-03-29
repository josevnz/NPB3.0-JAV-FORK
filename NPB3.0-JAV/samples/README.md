# How they where created?
* JAVA_HOME=$HOME/jdk-11.0.10 /usr/bin/numactl --physcpubind 1,2,3,4,5,6,7 ./testAllW > ./samples/testAllW-oraclejdk-11.0.10.txt
* JAVA_HOME=$HOME/graalvm-ce-java11-21.0.0.2 /usr/bin/numactl --physcpubind 1,2,3,4,5,6,7 JAVA_HOME=$HOME/graalvm-ce-java11-21.0.0.2 ./testAllW > ./samples/testAllW-graaljvm-11.0.10.txt
