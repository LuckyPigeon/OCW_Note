# Algorithm and Computation

Year: Spring 2020 <br />
Instructor: Prof. Erik Demaine <br />
Course Link: <https://www.youtube.com/watch?v=ZA-tUyM_y7s&list=PLUl4u3cNGP63EdVPNLG3ToM6LaEUuStEY&index=1/>

## Course Overview

### Goals

* Solve computational problems.
* Prove the correctness of your thinking.
* Argue with others about your solution’s efficiency.
* In general, it’s about communication of these ideas.

## Algorithm Overview

### What is a Problem

* They have inputs and corresponding outputs.
* Arbitrary size of inputs, but fixed size of outputs.

### What is an Algorithm

* Must be a function that for given inputs, produce expected outputs.

### Sample Algorithm Description

* For birthday problem (if there are at least two people share same birthday)
	
1. Maintain record.
2. Interview students in some order.
3. Check if birthday is recorded, if so, return pair.
4. Keep adding student to record.
5. Return none if don’t find any.

It’s a simple example of how algorithm works, when you explain this procedure to friends, they can 
understand what you’re going to do.
To make students, have a basic logic understand this idea, solve problems with induction,
 regression… etc., it’s crucial to ask students to take discrete mathematic before algorithm course.

### Induction

Need to use induction to scale the solution from limit size to large / infinite size and prove it.

* Induction Hypothesis: If first k students contain match, algorithm returns a match before 
interviewing student k+1.
* Base Case: k=0
* Assume: Induction Hypothesis k=0 for k=k^'
    * If k^'  contains a match, already return by induction.
    * If k^'+1 contains a match, check k^'+1 against all students.

### Efficiency

* Instead of measure time, we abstract the time works in machine out of picture and count 
fundamental operations.
* Expect performance to depend on size of your inputs.
* Have annotations.
    * Big O represents upper bound.
    * Omega Ω represents lower bound.
    * Theta θ represents both.
* Types of efficiency representation
    * O(1): constant time, always take same amount of time
    * O(lg n): logarithmic time
    * O(n): linear time
    * O(n lg n): linear logarithmic time
    * O(n^C): polynomial time

![Efficiency and Complexity](../../../Images/Introduction%20to%20Algorithms/Efficiency%20and%20Complexity.jpg)

### Model of Computation

* A “Word” in our RAM depends on our operating system (32 or 64 bits).
* “Word” represents how many possibilities that RAM can take, 2^32 or 2^64.
* 32 bits operating system roughly takes 4GB of possibilities.
* 64 bits operating system roughly take 20 Exabytes of possibilities. Total data that Google store 
is roughly 10 Exabytes, so we won’t run out of those possibilities in a short time.
* Those possibilities are store in RAM as addresses, which can be used by CPU.
* Addresses can be used to perform these operations in constant time.
    * Integer arithmetic
    * Logical operation
    * Bitwise manipulation
    * Retrieve value
