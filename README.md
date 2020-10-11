# Sprint Challenge: Hash Tables

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past sprint and apply them in a concrete project. This sprint explored hash tables. During this sprint, you studied hash functions, collision resolution, complexity analysis of hash tables, load factor, resizing, and various use cases for hash tables. In your challenge this week, you will demonstrate mastery of these skills by solving five problems related to hash tables.

The sprint challenge is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your TL if you need direction.

_You have **three hours** to complete this challenge. Plan your time accordingly._

## Introduction

This challenge requires you to solve algorithm problems that are amenable to being solved efficiently with a hash table.

### Commits

Commit your code regularly and meaningfully. This practice helps both you (in case you ever need to return to old code for any number of reasons) and your Team Lead as they evaluate your solution.

## Interview Questions

Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. You might prepare by writing down your answers beforehand.

1. Hashing functions

A hash function is a function where the input is any data, and the output is a number.A hash function must be consistent (deterministic). Every time it receives the same input, it must return the same output.
If it’s not deterministic, it is not a hash function.Different input data should return different numbers.
A hash function must return numbers that are within a specific range.When a hash function maps each different input data to a different number, it is called a perfect hash function.
There are different kinds of hashing functions
1)A Naive Hashing Function:Hashing functions take an input (usually a string) and return an integer as the output. To convert a string into an integer, hashing functions operate on the individual characters that make up the string.
2)Modulo:The modulo operator returns the remainder of dividing the left-hand operand and the right-hand operand. When the right-hand operand is greater than the left-hand operand, the modulo operator returns the value of the left-hand operand.
3)A Simple Hash Table:The simple hash table does not handle collisions.It can search, insert, and delete all in constant time (O(1)).

2. Collision resolution

Hash functions always map different inputs to different indexes. However, unless you knew all the possible data ahead of time,
it would be impossible to write a hash function that was perfect in this regard. In actuality, hash functions do occasionally return the same integer, given different inputs.

3. Performance of basic hash table operations

Once we take collisions into account with our hash tables, the performance implications are a bit different. Now,
in the worst case, search, insertion, and deletion operations take linear time (O(n)) and are not constant.
The worst case would be if every hash table entry were placed inside the linked list that was referenced by a single index.
However, the average case is still constant time (O(1)). So, if we handle collisions well and we have a hashing function that
does an excellent job of spreading the data evenly across the hash table, hash tables are very performant data structures.

4. Load factor

The load factor of a hash table is trivial to calculate. You take the number of items stored in the hash table divided by the number of slots.

Load Factor = Number of items in Hash Table
**\*\***\*\***\*\***\_\_\_**\*\***\*\***\*\***
Total Number of Slots
Hash tables use an array for storage, so the load factor would be the number of occupied slots divided by the length of the array.
If the load factor is too high or too low, then you need to resize.

5. Automatic resizing

As the load factor of your hash table increases, so does the likelihood of a collision, which reduces the performance of your hash table.
Therefore, you need to monitor the load factor and resize your hash table when the load factor gets too large.
The general rule of thumb is to resize your hash table when your load factor is greater than 0.7.
Also, when you resize, it is common to double the size of the hash table. When you resize the array,
you need to re-insert all of the items into this new hash table. You cannot simply copy the old items into the new hash table.
Each item has to be return through the hashing function because the hashing function takes into account the size of the hash table when determining the index that it returns.
You can see that resizing is an expensive operation, so you don’t want to resize too often.
However, when we average it out, hash tables are constant time (O(1)) even with resizing.
The load factor can also be too small. If the hash table is too large for the data that it is storing,
then memory is being wasted. So, in addition to resizing, when the load factor gets too high,
you should also resize when the load factor gets too low.

6. Various use cases for hash tables

1) Duplicate Prevention:

- storing users (prevents creating duplicate users or overwriting a user).
- a voting system (one person, one vote).
  2)Caching
  Servers use hash tables to cache the data and information they are serving down to clients.
  It doesn’t make sense to have the server run computations every time a client requests a page.
  Instead, the server runs the calculation the first time and then caches that information to serve to all the other clients that will ask for it.
  If the server gets updated information, you would then want the server to rerun the computations and cache the new result.
  Servers would be much less performant in their ability to serve high numbers of clients without being able to utilize caching with hash tables.
  The hash table, in this case, maps the URL that the client requests to the page data that it needs to send back to the client.

We expect you to be able to answer questions in these areas. Your responses contribute to your Sprint Challenge grade.

## Instructions

### Task 1: Project Set-Up

- [ ] Create a forked copy of this project
- [ ] Add your team lead as a collaborator on Github
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!)
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly
- [ ] Push commits: git push origin `<firstName-lastName>`

### Task 2: Project Requirements

Your finished project must include all of the following requirements:

- [ ] Solve any three of the five problems

For each problem that you choose to solve, complete the following:

- [ ] Navigate into each exercise's directory
- [ ] Read the instructions for the exercise in the README
- [ ] Implement your solution in the `.py` skeleton file
- [ ] Make sure your code passes the tests running the test script with make tests

_Note: For these exercises, we expect you to use Python's built-in `dict` as a hashtable. That said, if you wish, you can attempt to solve using your own hashtable implementation, as well. All solutions should utilize a `dict` or hashtable. You should not use Sets. (Though you can make a `dict` behave like a set if you wish.)_

### Task 3: Stretch Goals

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module, but they build on the material you just studied. Time allowing, stretch your limits, and see if you can deliver on the following optional goals:

- [ ] Solve any four of the five problems
- [ ] Solve all five problems

## Submission format

Follow these steps to complete your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's Repo). **Please don't merge your own pull request**
- [ ] Add your team lead as a reviewer on the pull-request
- [ ] Your team lead will count the project as complete after receiving your pull-request
