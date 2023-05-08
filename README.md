Download Link: https://assignmentchef.com/product/solved-ucs1411-exercise-8-memory-management-algorithms
<br>
Free space is maintained as a linked list of nodes with each node having the starting byte address and the ending byte address of a free block. Each memory request consists of the process-id and the amount of storage space required in bytes. Allocated memory space is again maintained as a linked list of nodes with each node having the process id, starting byte address and the ending byte address of the allocated space. When a process finishes (taken as input), the appropriate node from the allocated list should be deleted and this free disk space should be added to the free space list. [Care should be taken to merge contiguous free blocks into one single block. This results in deleting more than one node from the free space list and changing the start and end address in the appropriate node]. For allocation use first fit, worst fit and best fit algorithms.

<u>Steps:</u>

<ol>

 <li>Get the algorithm to work with. (First Fit, Best Fit, Worst Fit)</li>

 <li>Implement this using Linked List / Arrays.</li>

 <li>Let the options be 1. Entry / Allocate 2. Exit / Deallocate 3. Display ( Memory allocated LL, Free Pool LL, Total Physical memory by Merging 2 LL) 4.Coalescing Holes.</li>

 <li>Create a node using structure with the following details. Starting address, ending address, Size, Status ( contains process id or H to denote that it is a hole).</li>

 <li>Create a Alloted memory Linked list with a collection of nodes (Initially no nodes).</li>

 <li>Create a Free Pool Linked List with a collection of nodes (Initially all partitions will be in free pool LL).</li>

 <li>Get the memory representation as input from user. No of partitions, starting address and ending address of each partition. Calculate the Size of each partition. Initially all the partitions will be in free pool LL.</li>

 <li>Now get whether a process enters / exits.</li>

 <li>If ”Entry” then get the process id and its size in bytes. Using the algorithm allocate memory for it and store it in alloted memory linked list. Modify in Free pool Linked list also. [ delete from free pool LL, insert into memory allocation LL ]</li>

</ol>

10.If “exit” then get the process id and then deall ocate the process from memory allocation linked list and include it in free pool linked list. [delete from memory allocation LL, insert into free pool LL ]

11.On display you have to display both LL separately and combined memory structure should be displayed by merging both LL.

<sub>     </sub>Merged Output should be

<sub>       </sub>12.For Coalescing of Holes scan the free pool LL and check for continuous holes. Ifso merge them as single hole by modifying ending address and size and delete the other hole.

13.For first fit select the first hole that satisfies the memory request.

14.For best fit select the hole that is large enough to accommodate the process but incurs minimum wastage of memory.

15.For worst fit select the hole that is the largest.

<u>Sample Input and output:</u>

<sub>    </sub>Enter the Memory Representation:

<sub>   </sub>Enter the no. of partitions in memory : 5

<sub>   </sub>Starting and ending address of partition 1: 100 110

<sub>   </sub>Starting and ending address of partition 2: 110 112

………….




Alloted Memory LL —–&gt;  Null

<sub>      </sub>Free Pool &gt;

Physical Memory—&gt;

<sub>     </sub>Memory Allocation Algorithm:

<sub>      </sub>1.First Fit

<sub>      </sub>2.Best Fit

<sub>      </sub>3.Worst Fit

<ol start="4">

 <li>Exit from program Enter choice : 1</li>

</ol>

<sub>                                                                   </sub>First Fit Memory Allocation Algorithm

<sub>     </sub>1.Entry / Allocate

<ol start="2">

 <li>Exit / Deallocate</li>

 <li>Display</li>

 <li>Coalescing of Holes</li>

 <li>Back to Algorithm</li>

</ol>

Enter choice : 1

<sub>     </sub>Enter process id : P1

<sub>     </sub>Enter size needed : 5

Memory is alloted to P1

<sub>     </sub>Alloted Memory LL—- &gt;

<sub>                                                                   </sub>First Fit Memory Allocation Algorithm

<sub>     </sub>1.Entry / Allocate

<ol start="2">

 <li>Exit / Deallocate</li>

 <li>Display</li>

 <li>Coalescing of Holes 5. Back to Algorithm</li>

</ol>

Enter choice : 2

Enter process id : P1

Memory is deallocated.

Alloted Memory LL —-&gt; Null

<sub>      </sub>Free Pool —