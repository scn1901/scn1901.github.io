---
layout: essay
type: essay
title: "The Beauty of Javascript...?"
date: 2023-08-30
published: true
labels:
  - Essay
  - Homework
---

<img width="300px" class="rounded float-start pe-4" src="">

## The Beauty of Javascript...?

Javascript, the programming language of web applications, is used in over 90% of all websites and was said to be created in about 10 days. Who would expect such a well-known, frequently used programming language to be hated? Javascript enthusiasts, if they exist, may reason (don’t fall for it) that Javascript has interesting capabilities: “Javascript allows functions in first class!”, “Javascript makes it so we can create cool websites!”, insert Javascript praise here… Whoever you are, you may be in denial. I could create lists and arrays that give all the reasons to find Javascript unappealing and these lists would have time complexity O(n!) in all methods of sorting! 

## "Why?" You may ask.
Rhetoric aside, let us explore the challenges in the language of Javascript. 

First and foremost, comparisons between numbers and between numbers converted to string in Javascript. 
Javascript utilizes IEEE 754 Double Precision, which results in comparisons such as 0.1 + 0.2 === 0.3 to be false, 1.0000000001 === 1 to be true, and 9999999 == 10000000 to be true. With comparisons of arrays, 16 == [16] true, but 16 == [1,6] false and “1,6” == [1,6] true.


As for arrays, an empty array, arr, has a length of 0 but arr[3] is “undefined” where we would expect a bound exception. In addition, you can append values to values past the supposed length of the array i.e. using the previous example, arr[3] = “hi” is applicable and will have .length of 4. Deleting arr[3] will still result in a length of 4 when arr[3] is now “undefined”. 
```
>>> var arr = [];
>>> arr.length     // 0
>>> arr[3]         // "undefined"
>>> arr[3] = "hi";
>>> arr.length     // 4
>>> delete(arr[3]);
>>> arr.length     // 4
>>> arr[3]         // "undefined"
```

Although there are more functionalities of Javascript that may raise some eyebrows, we will end with the uncertainty of variables with no defined type (Javascript’s var). With example var i = 1, i = i + “” will make i a string, right? If we continue with the variable i and add 1, we get “11”, which could be reasoned as 1 is being added as a string, however, when i - 1, the result will be 0.
```
>>> var i = 1;
>>> i = i + "";
>>> i + 1       // "11"
>>> i - 1       // 0
```
# Conclusion
The unfortunate souls who utilize Javascript in their daily lives do not deserve such punishment. As I have said previously, we could list an endless number of reasons to dislike Javascript, however, these reasons should have been enough to open a programmer’s eyes to see the true nature of Javascript.

# Athletic Software Engineering
Speaking from the perspective of a student programmer who has been learning in classes and utilizing code in projects, I think athletic software engineering is a very effective method of learning. The WODs, so far, have been simple and straightforward, making it easy to practice the syntax as many of us may be writing in Javascript for the first time. The WODs may be stressful, but the stress doesn’t allow for us to idly complete the task given to us. An elementary/middle school teacher once told me that students will complete the task in whatever time is given to them, whether it be 10 minutes or an hour, they will complete it within the time you give them. Although she was referring to young children, I thought this statement was quite relevant to even us college students. Thus, the urgency of completing the WOD task helps me in keeping me focused, not only in training my brain to quickly think of a solution for the problem. It is also quite gratifying to complete a WOD in a shorter time than you would have expected (though I do not expect myself to do as such when the WODs become more complicated). This is not to say, however, that projects should have earlier due dates. Tasks like those in WODs are more concise and will allow us to practice a couple of Javascript strategies/functions, whereas projects require us to incorporate multiple strategies into one code.
