# Sets
A set is a list of data, except the order does not matter in a set like it does in a stack or queue.  Another quality about sets is they do not allow duplicates.  This no duplicates rule makes it simpler to store information since we do not care about order in a set.

# Hashing
Hashing is a technique we use to test the set to check if the data we're looking for is in the set.  Hashing is also used to add and remove from the data set.

    # hash for integer unchanged
    print('Hash for 181 is:', hash(181))
    # hash for decimal
    print('Hash for 181.23 is:',hash(181.23))
    # hash for string
    print('Hash for Python is:', hash('Python'))
    
    Output:
    Hash for 181 is: 181
    Hash for 181.23 is: 530343892119126197
    Hash for Python is: 3607259692854166150

# Open addressing and chaining
When we are using python, we use open addressing to handle collisions.  If we are trying to add something in a specific spot in our set, oped addressign will tell us that spot is occupied by another data value already.  We will then know to try the next spot.

![image](https://user-images.githubusercontent.com/75501838/207481128-27eca98e-cb4c-402a-bcdd-4faf5e17dc54.png)

Another mthod we use to handle collisions is called chaining.  Instead of telling us to use a different spot for our datda like how open addressign does, we use chaining to make another list of data that can all fit into the same spot.

# Example
Hashing example:
    result = hash(21) # integer value  
    result2 = hash(22.2) # decimal value
    
    output:
    21
    461168601842737174

Open addressing example:
    Hash-Insert(T, k)
        i = 0
        do
            j = h(k, i)
            if T[j] == NIL
	            T[j] = k
	            return j
            else
	            i = i + 1
        while i < m
    error "hash table full"

Example of chaining:
    class CalculatorFunctions(): 
        def sum(self): 
            print("Sum called") 
            return self 
        def difference(self): 
            print("Difference called") 
            return self 
        def product(self): 
            print("Product called") 
            return self 
        def quotient(self): 
            print("Quotient called")
            return self
    if __name__ == "__main__": 
        calculator = CalculatorFunctions()  
        calculator.sum().difference().product().quotient()
        
    Output:
    Sum called 
    Difference called 
    Product called 
    Quotient called

# Problem to solve
Write a Python program to find the length of a set.

# Solution
    #Create a set
    setn = {5, 10, 3, 15, 2, 20}
    print("Original set elements:")
    print(setn)
    print(type(setn))
    print("\nLength of the said set:")
    print(len(setn))

    setn = {5, 5, 5, 5, 5, 5}
    print("Original set elements:")
    print(setn)
    print(type(setn))
    print("\nLength of the said set:")
    print(len(setn))

    setn = {5, 5, 5, 5, 5, 5, 7}
    print("Original set elements:")
    print(setn)
    print(type(setn))
    print("\nLength of the said set:")
    print(len(setn))
