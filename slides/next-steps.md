##  Next Steps

<ul>
    <li class="fragment fade-in">
        Realistically, requires a more sophisticated Flume topology. 
    </li>
    <li class="fragment fade-in">
        Maintenance of the Hadoop cluster must be considered.
    </li>
    <li class="fragment fade-in">
        Not all logging frameworks supported out-of-the-box.
    </li>
    <li class="fragment fade-in">
        Must configure carefully.
    </li>
    <li class="fragment fade-in">
        Partitioning, Data
        <ul>
            <li>
                Re-partition ymd to y, m, d
            </li>
            <li>
                Add partitions for app, instance
            </li>
            <li>
                Parse XML to include other important data in schema?
            </li>
        </ul>
    </li>
    <li class="fragment fade-in">
        Automate the creation of Impala partitions.
    </li>
    <li class="fragment fade-in">
        Investigate Parquet
    </li>
    <li class="fragment fade-in">
        Investigate Kudu
    </li>
</ul>

note:
    * Topology: This works well for a single instance of a single application.
    * Maintenance: (e.g., purging, compacting, balancing, filesystem checks, etc.)
    * Logging Frameworks: Logback, etc.
    * Configuration: Balance between HDFS file size, rolling file size and interval, backpressure
    * Partitioning: We can add all sorts of data to help queries (session ID, etc.)
    * Automate partitioning: Oozie?
    