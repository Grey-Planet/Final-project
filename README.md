# Final-project
計算機組織-Final Project  
  
Q3: Config last level cache to 2-way and full-way associative cache and test performance  
<pre>
2-way:  
  &emsp;system.l3.overall_miss_rate::total           0.558349                       # miss rate for overall accesses  
  &emsp;system.l3.replacements                         301257                       # number of replacements  
full-way:  
  &emsp;system.l3.overall_miss_rate::total           0.519544                       # miss rate for overall accesses  
  &emsp;system.l3.replacements                         268730                       # number of replacements  
</pre>
  
Q4: Modify last level cache policy based on frequency based replacement policy  
> benchmark：quicksort
<pre>
- default:  
  &emsp;system.l3.overall_miss_rate::total           0.539996                       # miss rate for overall accesses  
  &emsp;system.l3.replacements                         263736                       # number of replacements  
  &emsp;system.tol3bus.snoop_fanout::total            1298844                       # Request fanout histogram  
- LFU:  
  &emsp;system.l3.overall_miss_rate::total           0.573261                       # miss rate for overall accesses  
  &emsp;system.l3.replacements                         315460                       # number of replacements  
  &emsp;system.tol3bus.snoop_fanout::total            1350568                       # Request fanout histogram
</pre>

Q5: Test the performance of write back and write through policy based on 4-way associative cache with isscc_pcm  
<pre>
- write back  
  &emsp;system.tol3bus.snoop_fanout::total            3419819                       # Request fanout histogram  
- write through  
  &emsp;system.tol3bus.snoop_fanout::total           45124901                       # Request fanout histogram  
</pre>
