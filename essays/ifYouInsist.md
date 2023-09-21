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

ECMA Script 6 (ES6) is definitely a good tool and syntax for organized code, readability, and maintainability, as stated by various coding tutorial platforms and many companies as well. It reminds coders to be aware of how their code is read. Establishing a habit of writing code that would be palatable, easier to understand, by coders in the future, preparing us for the future when we collaborate with other coders is a great concept in theory. Despite previous stereotypes or assumptions about programmers, in the workforce, programmers must be good collaborators. Thus, it is necessary for code to not be straight 'code-vomit'.

I must admit, ES6 is very useful for beginner coders. Although it may be irritating in the beginning, it would become much easier to write constant good code once the habit is established. HOWEVER, a programmer who has coded for more than 2 years (estimate), may find the syntax more than a nuisance. Since I have been coding for more than 4 years, I have established my own rules while coding. My own syntax, if you will, that I find is the most organized. An example of this is function curly braces. Some people like to have the curly praces in a new line, however, I find it cleaner to have the first braces on the same line as the function. In addition, I am particular of my variable names. Constants will be all caps and use underscores while regular variables (int, double, etc.) will be in camelCase. 

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