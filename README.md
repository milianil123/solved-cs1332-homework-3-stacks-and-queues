Download Link: https://assignmentchef.com/product/solved-cs1332-homework-3-stacks-and-queues
<br>
You are to code the following:

<ol>

 <li>A stack backed by a singly-linked list</li>

 <li>A stack backed by an array</li>

 <li>A queue backed by a singly-linked list with a tail reference</li>

 <li>A queue backed by an array</li>

</ol>

A queue is a first-in, first-out (FIFO) data structure; the first item inserted is the first item to be removed. A stack is a last-in, first-out (LIFO) data structure; the last item to be inserted is the first item to be removed.

All of your data structures should meet the requirements stated in each of the method javadocs. The array classes have a provided INITIAL CAPACITY; make sure to use the provided variable, not a magic number. Your linked list implementations should use the given head (and tail) pointer(s) to build the backing structure. Do NOT use Java’s linked list classes.

As always, these implementations must be as efficient as possible and correspond to what was taught in class.

Circular Arrays

The backing array in your ArrayQueue implementation must behave circularly. For this assignment, the front variable in ArrayQueue should represent the index that holds the next element to dequeue. <strong>Failure to adhere to this may result in large penalties.</strong>

For enqueuing, add to the back of the queue. To access the back of the queue, you can add the size to the front variable to get the next index to add to, though you will have to account for the circular behavior yourself.

When the user dequeues an element, you should simply treat the next index in the array as the new front. <strong>DO NOT SHIFT ANY ELEMENTS IN THE ARRAY DURING A DEQUEUE. </strong>This also means that if there are empty spaces at the front of the array, the back of the queue should wrap around to the front of the array and make use of those spaces.

When regrowing the backing array, realign the queue with the front of the new array during transfer, so that the front of the queue is once again at index 0.

Additionally, after removing the last element in the queue, reset the front variable to the beginning of the array, index 0.