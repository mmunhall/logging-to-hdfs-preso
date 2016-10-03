##  Design Goals

<ul>
    <li class="fragment fade-in">
        Reduce the amount of log data stored on a filesystem
    </li>
    <li class="fragment fade-in">
        Reduce the amount of file IO and disk thrash
    </li>
    <li class="fragment fade-in">
        Continue to allow logs to be written to the filesystem
    </li>
    <li class="fragment fade-in">
        Store all log data in Hadoop for analysis
    </li>
    <li class="fragment fade-in">
        Allow for old data to be purged
    </li>
    <li class="fragment fade-in">
        Monitor log data in near real time
    </li>
    <li class="fragment fade-in">
        Allow for the data to be analyzed programmatically (e.g. map/reduce, Spark, _[insert buzzword]_)
    </li>
</ul>
        

note:
    * Demo: Start at the end
