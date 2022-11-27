# Queue
When discussing Queues, we are going to start with learning the differences between LIFO and FIFO.  We will also learn how to implement the FIFO method using python.

# LIFO
LIFO is short for last in first out.  LIFO is used when implementing stack, it is not used when implementing a queue.  Although, it is good to know what LIFO is when learning about queues.  When we are using LIFO in a list, the first item we remove is the last item in the list.  We implement this in python by using the push and pop commands.  Using LIFO is a good way to easily modify your lists when using python.

# FIFO
FIFO is the complete opposite of LIFO.  It stands for first in first out.  Versus LIFO, where we are taking the last item out of the list, for FIFO we are taking the first item out of the list.  A good real life example of this is a reservation list at a restaraunt.  Typically, when a restaraunt takes reservations, the person at the top of the list gets seated first, no matter how long other people have been waiting.  Just like this, the fist item we have in our list is the first item to get removed from the list ot be "seated."

Example:
Lets say we have a list here of people waiting to be seated at a restaraunt.

        Joan, Bidgett, Alex, Shephanie, John, Garrett

We have one table available, so Joan will be seated first and then removed from the list.  Our new list shows as follows:

        Bridgett, Alex, Stephanie, John, Garrett

A few minutes go by and we now have three tables available.  This means we can now seat the next three people in our list, starting with Bridgett:

        John, Garrett
        
As you can see in this example, the first item in the list will always be the first item removed when using FIFO.

In python, we will use the commands dequeue and enque.  Dequeue is used to remove the first item in the list.  Enqueue is used to add another item to the list, this will add the item at the end of the list.

Python example:

    #Here, we are adding items to our list by using enqueue
    queue.enqueue("Joan")
    queue.enqueue("Bridgett")
    queue.enqueue("Alex")
    queue.enqueue("Stephanie")
    queue.enqueue("John")
    queue.enqueue("Garrett")

    #Here, we are removing items form our list by using dequeue
    result = queue.dequeue()
    print(result)
    result = queue.dequeue()
    print(result)
    result = queue.dequeue()
    print(result)
    result = queue.dequeue()
    print(result)
    
# Problem to Solve
Your friend asks you if you can help them out with their business by making a program that will help them keep track of their incoming and completed orders.  You know using a queue will probably be the best option to help your friend out.
 
 For this problem, you will need to make a program that uses a queue to keep track of what orders your friend has completed and not completed.  Use the following information in your test cases:
 
    On September 11 - a new order came in
    September 28 - new order came in
    October 19 - new order came in
    December 10 - new order came in
    January 1 - Dec 10 order was completed
    January 2 - Oct 19 order was completed
    
You can check you code here: "still completing solution, will add here when complete."
