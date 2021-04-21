Dean Chung
Michael Catterall
Michael Jones
  
  5.6.1 Python:
  
1. What is the type of collection used in the exercise?  
  Queue
2. What are the different ways of iterating through a collection?  
  For, Map, Filter, While,
3. How do you find out the size of a collection?  
  fifoLength >> q.qsize() 
4. How do you add an item to a collection? What happens if you try to add an item to a collection that is already full? 
  fifoEnqueue >> q.put()
5. How do you remove an item to a collection? What happens if you try to remove an item that does not exist in the collection?  
  Using .get() will remove by FIFO, and return it. 
  If the item does not exist, .get() will wait for it to be avilable unless a timeout is specified.
6. Change the implementation of a FIFO queue to a LIFO queue in 5.6.1.  
  
  ```
  # // use python queue
from queue import LifoQueue

# Initialise a queue
miqVoucherQ = LifoQueue(maxsize = 100)

# NB: Assume we do not know about objects in python, so create functions insteand

# define a function to add to end of queue
def lifoEnqueue(queue,item):
  return queue.put(item)
  
# define a functiion to remove from front of queue
def lifoDequeue(queue):
    return queue.get();
  
# define a function to find queue length
def lifoLength(queue):
    return queue.qsize()
    
# define a function to find if queue is empty
def lifoIsEmpty(queue):
    return queue.empty()
    
print(lifoLength(miqVoucherQ))
print(lifoIsEmpty(miqVoucherQ))

# Add some travellers
lifoEnqueue(miqVoucherQ,["Jones, E","10","10-01-2021","20-01-2021"])
lifoEnqueue(miqVoucherQ,["Amed, J","1","11-02-2021,20-02-2021"])
lifoEnqueue(miqVoucherQ,["Vine, M","8","9-01-2021,21-09-2021"])

# Show queue length, isEmpty
print(miqVoucherQ);
print(lifoLength(miqVoucherQ));
print(lifoIsEmpty(miqVoucherQ));

# remove from the queue and make sure LIFO
lifoDequeue(miqVoucherQ)
print(lifoLength(miqVoucherQ));
```

  5.6.1 Javascript:

1. What is the type of collection used in the exercise?  
  
2. What are the different ways of iterating through a collection?  
  
3. How do you find out the size of a collection?  
  
4. How do you add an item to a collection? What happens if you try to add an item to a collection that is already full?  
  
5. How do you remove an item to a collection? What happens if you try to remove an item that does not exist in the collection?  
  
6. Change the implementation of a FIFO queue to a LIFO queue in 5.6.1.  
  
