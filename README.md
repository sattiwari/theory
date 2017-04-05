# Theory

## Disk


## Networking
* TCP Window Scaling

## G1 Garbage Collection
* Automatically adjusts to different workloads and provided consistent pause time for garbage collection over the lifetime of the 
application
* handles large heap sizes with ease, by segmenting the heap into smaller zones and not collecting over the entire heap in each 
pause
* MaxGCPauseMillis - preferred pause time for each garbage collection cycle. It is not a fixed maximum - G1 can and will exceed 
this time if it is required. This value defaults to 200 milliseconds. This means that G1 will attempt to schedule the frequency
of GC cycles, as well as the number of zones that are collected in each cycle, such that each cycle will take approximately 200ms.
* InitiatingHeapOccupancyPercent: This option specifies the percentage of the total heap that may be in use before G1 will 
start a collection cycle. The default value is 45. This means that G1 will not start a collection cycle until after 45% of the 
heap is in use. This includes both the new (eden) and old zone usage in total.
* The start script of Kafka uses Parallel New and Concurrent Mark and Sweep garbage collection 

More details - http://www.oracle.com/technetwork/tutorials/tutorials-1876574.html
