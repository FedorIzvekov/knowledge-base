[Return to main README.md](../README.md#knowledge-base)

# Performance

## Latency Comparison Numbers

| Operation                                       |     ns      |   μs    |     ms      |
|-------------------------------------------------|:-----------:|:-------:|:-----------:|
| L1 cache reference                              |     0.5     | 0.0005  | 0.000 000 5 |
| Branch mispredict                               |      5      |  0.005  |  0.000 005  |
| L2 cache reference                              |      7      |  0.007  |  0.000 007  |
| Mutex lock/unlock                               |     25      |  0.025  |  0.000 025  |
| Main memory reference                           |     100     |   0.1   |   0.000 1   |
|                                                 |             |         |             |
| Compress 1 KB (Zippy)                           |   20 000    |   20    |    0.02     |
| Read/Write 1 MB sequentially from/to memory RAM |   50 000    |   50    |    0.05     |
| Read/Write 1 MB random from/to memory RAM       |   300 000   |   300   |     0.3     |
| Read 1 MB sequentially from NVMe SSD            |   500 000   |   500   |     0.5     |
| Read 1 MB sequentially from SATA SSD            |  1 000 000  |  1 000  |      1      |
| Read 1 MB sequentially from HDD                 |  2 000 000  |  2 000  |      2      |
| Read 1 MB random from NVMe SSD                  |  2 000 000  |  2 000  |      2      |
| Read 1 MB random from SATA SSD                  |  4 000 000  |  4 000  |      4      |
| Disk seek                                       | 10 000 000  | 10 000  |     10      |
| Read 1 MB random from HDD                       | 50 000 000  | 50 000  |     50      |
|                                                 |             |         |             |
| Round trip within same datacenter               |   500 000   |   500   |     0.5     |
| Round trip Western Europe -> US Central         | 120 000 000 | 120 000 |     120     |
| Round trip US California -> Netherlands         | 150 000 000 | 150 000 |     150     |
| Round trip Western Europe -> Singapore          | 180 000 000 | 180 000 |     180     |

## Data Structures Time and Space Complexity

| **Data Structure**                       |              **Average Time Access**               |    **Average Time Search**    |  **Average Time Insertion**   |   **Average Time Deletion**   |     **Worst Time Access**     |     **Worst Time Search**     |   **Worst Time Insertion**    |    **Worst Time Deletion**    |  **Worst Space Complexity**   |
|:-----------------------------------------|:--------------------------------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|
| **Array / Array List**                   |             <instant> Θ(1) </instant>              | <efficient> Θ(n) </efficient> | <efficient> Θ(n) </efficient> | <efficient> Θ(n) </efficient> |   <instant> O(1) </instant>   | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> |
| **Linked List**                          |           <efficient> Θ(n) </efficient>            | <efficient> Θ(n) </efficient> |   <instant> Θ(1) </instant>   |   <instant> Θ(1) </instant>   | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> |   <instant> O(1) </instant>   |   <instant> O(1) </instant>   | <efficient> O(n) </efficient> |
| **Hash Table / Hash Map / Hash Set**     |                        N/A                         |   <instant> Θ(1) </instant>   |   <instant> Θ(1) </instant>   |   <instant> Θ(1) </instant>   |              N/A              | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> |
| **Red-Black Tree / Tree Map / Tree Set** |                        N/A                         |    <fast> Θ(log n) </fast>    |    <fast> Θ(log n) </fast>    |    <fast> Θ(log n) </fast>    |              N/A              |    <fast> O(log n) </fast>    |    <fast> O(log n) </fast>    |    <fast> O(log n) </fast>    | <efficient> O(n) </efficient> |
| **Queue**                                | <efficient> Θ(n)</efficient><br>* no random access | <efficient> Θ(n) </efficient> |   <instant> Θ(1) </instant>   |   <instant> Θ(1) </instant>   | <efficient> O(n) </efficient> | <efficient> O(n) </efficient> |   <instant> O(1) </instant>   |   <instant> O(1) </instant>   | <efficient> O(n) </efficient> |
| **Stack / Deque**                        |             <instant> Θ(1) </instant>              | <efficient> Θ(n) </efficient> |   <instant> Θ(1) </instant>   |   <instant> Θ(1) </instant>   |   <instant> O(1) </instant>   | <efficient> O(n) </efficient> |   <instant> O(1) </instant>   |   <instant> O(1) </instant>   | <efficient> O(n) </efficient> |

<style>
instant{background:green;color:black;}
fast{background:lightGreen;color:black;}
efficient{background:yellow;color:black;}
normal{background:orange;color:black;}
</style>