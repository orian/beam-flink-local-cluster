# beam-flink-local-cluster
trivial flink local cluster project

This is super simple project with fatjar, to compile:

    mvn clean package
    
To run, start local flink cluster using:
    
    $FLINK/bin/start-local.sh
    
Download the text file:
    
    curl http://www.gutenberg.org/cache/epub/1128/pg1128.txt > /tmp/kinglear.txt

To run the jar:
    
    flink run target/dataflow-test-1.0-SNAPSHOT.jar \
      --runner=org.apache.beam.runners.flink.FlinkRunner \
      --input=/tmp/kinglear.txt --output=/tmp/wordcounts.txt
