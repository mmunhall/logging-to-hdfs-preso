# Logging to HDFS

note:
    * Original driver: Reduce disk thrash and file IO, especially because of increased logging with Kafka.
    * Additional benefits regardless of Kafka.
    * Traditional use case for Hadoop, which we have and are not fully utilizing yet.
    * Traditional, proven technologies and techniques.
    * Minimal impact to existing Canoe applications.