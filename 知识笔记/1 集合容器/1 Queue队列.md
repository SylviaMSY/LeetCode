# Queue 队列

Interface Queue<E>

- Suerinterfaces：[Collection](https://docs.oracle.com/javase/7/docs/api/java/util/Collection.html)<E>, [Iterable](https://docs.oracle.com/javase/7/docs/api/java/lang/Iterable.html)<E>

- Subinterfaces：[BlockingDeque](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/BlockingDeque.html)<E>, [BlockingQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/BlockingQueue.html)<E>, [Deque](https://docs.oracle.com/javase/7/docs/api/java/util/Deque.html)<E>, [TransferQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/TransferQueue.html)<E>

- Implementing Classes：[AbstractQueue](https://docs.oracle.com/javase/7/docs/api/java/util/AbstractQueue.html), [ArrayBlockingQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/ArrayBlockingQueue.html), [ArrayDeque](https://docs.oracle.com/javase/7/docs/api/java/util/ArrayDeque.html), [ConcurrentLinkedDeque](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/ConcurrentLinkedDeque.html), [ConcurrentLinkedQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/ConcurrentLinkedQueue.html), [DelayQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/DelayQueue.html), [LinkedBlockingDeque](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/LinkedBlockingDeque.html), [LinkedBlockingQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/LinkedBlockingQueue.html), [LinkedList](https://docs.oracle.com/javase/7/docs/api/java/util/LinkedList.html), [LinkedTransferQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/LinkedTransferQueue.html), [PriorityBlockingQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/PriorityBlockingQueue.html), [PriorityQueue](https://docs.oracle.com/javase/7/docs/api/java/util/PriorityQueue.html), [SynchronousQueue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/SynchronousQueue.html)

  

## 1 Queue<E> 方法说明

|             | **Throws exception** | **Returns special value** |
| ----------- | -------------------- | ------------------------- |
| **Insert**  | add(e)               | offer(e)                  |
| **Remove**  | remove()             | poll()                    |
| **Examine** | element()            | peek()                    |

#### 来自Collection<E>的方法：

``` java
addAll、clear、contains、containsAll、equals、hashCode、iterator、remove、removeAll、size、toArray
```



## 2 Queue 子接口

#### Deque 双端队列：同时支持FIFO、FILO

实现类：

- ArrayDeque
- LinkedList



## 3 Queue 实现类

#### PriorityQueue 优先级队列

- 非FIFO，可以自定义排序方式