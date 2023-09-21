---
layout: essay
type: essay
title: "TMy code is pretty, how dare you."
date: 2023-08-30
published: true
labels:
  - Essay
  - ES6
---

<img width="300px" class="rounded float-start pe-4" src="/img/essay/es6Img.jpeg">

E28

I believe some coding standards can actually help you learn a programming language. Do you agree?
After your first week of using ESLint with IntelliJ, what are your impressions? Are you finding that getting the green checkmark is painful, or useful, or both, or something else entirely?


I cannot deny the fact that there will be benefits to coding with ESLint. But does coding have to be so excruciating? Something as small as a space before a function curly braces?

If you must see evidence of my frustration, let’s take a look at the command line for one of my working jsfiddle assignments after running npm run lint.

```
	✖ 59 problems (59 errors, 0 warnings)
  53 errors and 0 warnings potentially fixable with the `--fix` option.
```
### My code is pretty, don’t tell me otherwise.
I would like to think my coding style is always ‘pretty’. And if not pretty, I would like to think my code is easy to read. There is no way more than half of my code has coding standard errors. I honestly don’t see the problem with no spacing between the function argument parenthesis and the curly braces. If a person is viewing code and the spacing between curly braces confuses said person, they should be the one to understand that there is nothing wrong with this syntax.

(Disclaimer: This is rhetoric, I do not harbor such strong emotions about this…)

```
  40:31  error  Missing space before opening brace                                                      space-before-blocks
  41:33  error  Missing space before function parentheses                                               space-before-function-paren
  44:16  error  A space is required after ','                                                           comma-spacing
  52:36  error  Missing space before opening brace                                                      space-before-blocks
  72:41  error  Operator '-' must be spaced                                                             space-infix-ops
  72:45  error  Operator '+' must be spaced                                                             space-infix-ops
```

All these ‘errors’ are different errors that were displayed after running lint on my code. I find this quite absurd.

```
function sumRecursion(nums) {
  if (nums.length !== 0) {
    return nums[0] + sumRecursion (nums.slice(1));
  }
}

function sumTheSimpleWay(nums){
  return _.reduce(nums, function(memo, num){ return memo+num }, 0);
}

const nums = [1,2,3,4,5];
console.log(sumRecursion(nums));
console.log(sumTheSimpleWay(nums));
```

Does this code look disorganized to you? (If you say yes, you are wrong)
This code has no places for discrepancies! Tell me where would need to be changed? If you know ES6, you may not answer.