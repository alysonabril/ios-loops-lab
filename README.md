# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

var range1 = 1...150
for number in range1 {
print(number)
}
***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

var range2 = 142..<159
for number in range2 {
print (number)
}

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**
var range3 = 15...80
for number in range3 where number % 2 == 0 {
print(number)
}

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

var range4 = 19...51
for number in range4 where number % 2 == 1 {
print(number)
}

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

var range5 = 1..<100
for number in range5 where number % 10 == 5 {
print(number)
}

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

var range6 = 1...40
for number in range6 where number % 10 == 7 {
print(number)
}

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

for i in 10...150 where i % 3 == 0 {
print(i)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
var someRange = 20...150
for i in someRange where i % 2 == 0 && i % 3 == 0 {
print(i)
}

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`
var range = 20...150

for number in range where number % 10 == 4 {
print(number)
}

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
infintitely, there is no condition that tells the code when to stop
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
    if i == 9 {
    break
}
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
i += 1
if i == 1005 {
print(i)
break
}
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
if i == 1005 {
break
}
if i % 2 == 0 {
print(i)
}
i += 1
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
the first loop is a while loop, the second is a repeat while loop. The while loop states it's condition on the first line before opening the code block, and the repeat while loop states it's condition on the just after the last curly brace of the code block.  Their outputs will be the same because  their are the same, just listed differently.  They will both begin with "i = 1" and then end with "i = 10"
***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

Break tells the program should immediately stop a piece of code from recurring infinitely.  Continue tells the program that the code has finished iterating through the first loop, so it will stop and start the next iteration. 
***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[]1****
[]2****
[]3****
[]4
[]5
[]6
[]7
[]8******
[]9******
[]10*****

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[]1*****
[]2****
[]3*****
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2 {
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
the output will be:
"x = \(1), y = \(1)"
"x = \(2), y = \(1)"
"x = \(3), y = \(1)"

the innerloop will not go past 1 because it's condition (if y == 2) was met so i has executed the "continue" which tells the program to stop there and just continue the outerloop.
***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.


var range = 0...10

for x in range {
for y in range {
let tuple = (x,y)
print(tuple)
}
}


***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

var myRange = 0...10
for x in myRange {
for y in myRange where y == x + 5 {
let tuple = (x,y)
print(tuple)
}
}
***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```

var N = 5
var numSquared = 1

while numSquared <= N {
print(numSquared * numSquared)

numSquared += 1
}

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.


var N = 3


for _ in 1...N {
for _ in 1...N {
print("*", terminator: "")
}
print("")
}

***
