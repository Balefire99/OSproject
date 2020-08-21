name: Manaaz Riyas
matric number: 1818665
section: 4


input given: 

ccode     duration     priority    arrival_time     p_id    burst_time
2201        3             2            1              1         21
3401        2             3            2              2         3
1103        1             1            3              3         6
1156        2             4            1              4         2
2065        2             3            3              5         5


fcfs scheduling output:

processes       burst time     waiting_time      turn_around_time
    1               21              0                   21
    2               3               21                  24
    3               6		    24                  30
    4               2               30                  32
    5               5               32                  37

average waiting time: 21.4
average turn-around time: 28.8
order of scheduling: 1)2201 2)3401 3)1103 4)1156 5)2065

fcfs algorithm is the easiest to implement. it just puts all the processor requests
in a queue and executes them in order on  a first come, first serve basis. starvation will
never occur as every process will get it"s chance to run. however, if a process
executes for a very long time, then the processes at the very back of the 
queue will have to wait for a long time before they get a chance to be executed.

Although, being the easiest to implement, fcfs comparitively has the worst average
waiting time and average turn around time.


sjf scheduling output:

processes       burst time     waiting_time      turn_around_time
    1               21              16                  37
    2               3               1                   4
    3               6		    8                   14
    4               2               0                   2
    5               5               3                   8

average waiting time: 5.6
average turn-around time: 13
order of scheduling: 1)2201 2)1156 3)3406 4)2065 5)1103

In sjf, short processes are executed first before longer processes. the throughput
is higher than fcfs because more processes can be ececuted in less time.
however, long processes will have more waiting time and may suffer starvation.

sjf has comparitively a much lower average waiting time and average turn
around time and seems to be the best option out of all the three 
algorithms.

priority scheduling output:

processes       burst time     waiting_time      turn_around_time
    1               21              0                   2
    2               3               2                   5
    3               6		    5                   10
    4               2               10                  31
    5               5               31                  37

average waiting time: 9.6
average turn-around time: 17
order of scheduling: 1)1156 2)3401 3)2065 4)2201 5)1103

In priority scheduling, processes are executed based on priority. if a
new process arrives with a higher priority than the current running process,
the incoming process is put at the head of the ready queue, which means after
the execution of the current process it will be processsed.

priority scheduling has significantly lower average waiting time and average
turn around time than fcfs but is still higher than sjf.



