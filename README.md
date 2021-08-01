# Class 1

## Arrays
An array is a data structure that contains a group of elements. Typically these elements are all of the same data type, such as an integer or string.
Arrays are commonly used in computer programs to organize data so that a related set of values can be easily sorted or searched,
each identifed by at least one array index or key. The index of an array of size N can range from 0 to N-1.

Note: Python does not have built-in support for arrays, but Python Lists can be used instead.

Create an array containing fruit names:

    fruit = ['banana', 'orange', 'mango']
    
Access a single element of array:

    m = fruit[0]
    
Modify the value of the first array item:

    fruit[0] = 'guava'
    
Use the len() method to return the length of an array

    l = len(fruit)
    
You can use the for in loop to loop through all the elements of an array. Print each item in the fruit array:

    for m in fruit:
        print(m)
 You can append element to array by using :
 
      m.append("apple")
      
      
## Time Complexity
Time complexity is the amount of time taken by an algorithm to run, as a function of the length of the input.
It measures the time taken to execute each statement of code in an algorithm.

Note: The algorithm that performs the task in the smallest number of operations is considered the most efficient one in the terms of the time complexity.

## Space Complexity
The space complexity of an algorithm or a computer program is the amount of memory space required to solve an instance of the computational problem as a
function of characteristics of the input. It is the memory required by an algorithm until it executes completely.

## Complexity Chart
![Alt Text](https://camo.githubusercontent.com/958f45f6de25ef5d8606c372efef96a87e37b8701f854deb9a4951a7e385a444/68747470733a2f2f692e6962622e636f2f72346b325467532f74696d65636f6d706c65782e6a7067)

### Linear Search
Assume we have an given array and a value. Now we have to find the value in the array

    numbers = [3, 5, 8, 7, 4]
    target = 4

    for number in numbers
        if number == target
            print("found")
   
Here we need 5 operations to get the target value. These are the maximum number of operations for the array, in the case of Linear search,
this is also known as the worst case of an algorithm.

From this, we can conclude that the number of operations will be the same as the length of the array in the worst case.
When the length of array is n, thime complexity will be O(n)

Now we want to reverse the given array

    numbers = [3, 5, 8, 7, 4]
    result = []
    start = len(numbers) - 1

    while(start>=0)
        result.append(numbers[start])
        start-= 1 
    return result
Here this while loop will run n times , where n is equal to the length of the array.
So, number of operations will be n and the time complexity will be O(n). 
Beside this we need a new array (result) which has same number of elements as numbers array. For this, the space complexity will be O(n).

Now Let's improve our solution:

    numbers =  [3, 5, 8, 7, 4]
   
    start = 0
    end = len(numbers) - 1

    while(end>start)
        temp = numbers[end]
        numbers[end] = numbers[start]
        numbers[start] = temp
        end = end - 1
        start = start + 1

    return numbers
    Here we don't need extra array, memory space remain constant. Memory complexity will be O(1).
    While loop will run n/2 times where length of the array is equal to the n. So the complexity will be O(n/2).
    
    
