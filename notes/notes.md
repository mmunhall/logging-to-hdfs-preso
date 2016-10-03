

IDEA: START AT THE END!
=======================

















Design Goals
------------

* Reduce or eliminate completely the amount of log data stored on a filesystem,
* Reduce or eliminate the amount of file IO on a filesystem,
* Continue to allow logs to be written to the filesystem,
* Store all log data in Hadoop for analysis,
* Allow for old data to be purged,
* Provide an interface to monitor log data in near real time,
* Allow for the data to be analyzed programmatically (e.g. map/reduce, Spark, [insert buzzword])

Why this is a win/win for Canoe
-------------------------------

* We have a Hadoop environment.
* Our Hadoop environment is underutilized.
* Can run side-by-side with existing logging to disk.
* Very easy to implement with minimal changes to existing systems.

Architecture Overview
---------------------

Make pretty pictures

Next Steps
----------

* This works for a single instance of a single application, but anything more complex would require a different, potentially more complex Flume topology.
* Maintenance of a Hadoop cluster (e.g., purging, compacting, balancing, filesystem checks, etc.) is not mentioned, but must be considered.
* Is there a Logback Flume appender?
* Configuration
    * Memory flume channels are great for testing, but in production file channels should probably be used instead.
    * Roll interval, roll size and a number of other properties should be adjusted or specified to avoid a "small files" problem.
* Parititioning
    * Re-partition ymd to y, m, d
    * Add partitions for app, instance
* Automate the creation of Impala partitions. Is this a job for Oozie?
* Investigate Parquet
* Investigate Kudu

Technologies
------------

HDFS
Java log4j appender
Flume
Avro
Impala

What are We Doing Here?
-----------------------

Craig said, "..."

















fdsafdas















fdsafdas











fddfa
