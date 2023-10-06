# HPC_Assignment_2 
***Created a concurrent double-linked list (sorted list) using the following synchronization techniques:

1. Coarse-grain Synchronization
2. Fine-grain Synchronization
3. Optimistic Synchronization
4. Lazy Synchronization
5. Non-blocking Synchronization

Verified the performance of the concurrent data structure for different problem sizes (2 × 1000, 2 × 10000, and 2 × 100000) by varying the number of threads (1, 2, 4, 6, 8, 10, 12, 14, and 16) and workloads (0C-0I-50D, 50C-25I-25D, and 100C-0I-0D).

### 1. Coarse-grain Synchronization
Coarse-grained synchronization involves locking the entire data structure (in this case, the entire doubly linked list) to protect it from concurrent access. When one thread acquires the lock, it has exclusive access to the entire list, preventing other threads from accessing it until the lock is released.

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/077f517a-2474-454b-888f-8e4e58aa40ec)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/bacaebe3-9555-44c7-878a-7ba3973b3a55)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/47774f6b-7d01-4078-9696-841708afb67c)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/8ba064c1-728c-4fb5-9643-8c58a77577bf)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/bff6c2f7-0715-41e2-903c-b28d0f519da6)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/d349542a-47c5-4beb-903f-27d74fd9c7e7)

### 2. Fine-grained synchronization
Fine-grained synchronization divides the doubly linked list into smaller, independently locked sections. Each section (e.g., a node or a group of nodes) has its lock. Threads can operate concurrently on different sections, reducing contention.

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/87e49252-f53d-4c51-9b0a-587e0bd2513e)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/49f21bbe-f609-48b1-8f7f-c01d11ee1228)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/5d152346-6d9f-47ce-8f70-f349f9425501)

### 3. Optimistic Synchronization
Optimistic synchronization assumes that conflicts between threads are rare. Instead of locking data structures, each thread reads and makes modifications locally. Before applying changes, the thread validates that no other thread has modified the same data. If conflicts occur, the thread retries the operation.

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/6967a0fc-423d-4050-a829-d8291576839f)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/ae7411fe-7ffa-4c5b-874c-6d005eb55739)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/1b4376e8-ba1d-4512-b73d-4a2bd165af4d)

### 4. Lazy Synchronization
Lazy synchronization aims to delay synchronization until absolutely necessary. Threads perform operations without initially acquiring locks. Only during critical sections or when conflicts are detected are locks acquired to ensure data consistency.

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/e73bf8f6-ec8b-4047-9042-971ea01f48ce)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/8dc399af-f130-43f3-9be6-04453fa49faa)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/3a6dd3b8-d611-48da-b2fa-1920148a0621)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/549a3e80-f916-4220-b58e-029df3a48004)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/2aab080d-c8ed-409f-9da8-d0bb51c351dc)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/554140c9-e555-4649-a59f-d2ca5eb49ea0)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/e913574b-46e7-4c0f-9e2d-12f7c925ec64)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/15fc6216-9f10-4fac-8c0a-65e0a52cd349)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/97df9554-9aaa-4597-9556-2819c36aaf82)


### 5. Non-blocking Synchronization
Non-blocking synchronization techniques aim to eliminate the use of locks entirely. Instead, atomic operations, such as compare-and-swap (CAS), are used to modify data structures in a thread-safe manner. If a CAS operation fails due to a concurrent modification, the thread retries the operation.

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/c89c5620-00d6-4938-ab21-052949f66473)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/7418a9d0-b260-4019-9113-bd6135a3d2bd)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/471f4b27-a252-4341-b4be-2e43c061238a)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/57b58903-f250-4166-8262-0e5b3fa7d6ee)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/798cf9f9-6d3e-4594-8079-328bba4e8e25)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/bdd7c898-5867-4292-a525-025698d8172d)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/b976ab90-b8ec-410e-8d75-f9147ccd055e)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/15e9047b-5473-438d-a029-c121dc04fbab)

![image](https://github.com/ganeshvarmapotturi/hpc_assignment-2/assets/69681358/ba04c8ec-8cf1-4d0d-8c1e-d10cefec4ccf)

NOTE: In some techniques for a problem siza 3 individual graphs are plotted due to different range of throughput for each workload.
