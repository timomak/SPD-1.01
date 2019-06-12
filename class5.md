# Test Cases
Slides [link](https://docs.google.com/presentation/d/1zNb6jqB9NHmvlRY_cSyUqJA4gsHXg-IjfM1g0WmoPgs/edit#slide=id.g58d3d40430_0_0)

### Warm up
* **Good/Normal Input** - Input that you expect the user to give.
* **Bad/Unusual Input** - Input that you expect the user not to give.
* **Edge Case Input** - Input that you do not expect.

# In Class Practice

> For each one of the challenges, write down good, bad and edge case inputs.

1. Find the k largest values in an array of n numbers. Return them in a new array sorted in decreasing order.
  * **Normal**
    * [2, 8, 11, 7, 12, 0.0e1, -0.123123]
  * **Unusual**
    * [-2, -2, 8, 7, -7, 8, NaN, +Inf, "0", -0]
  * **Edge Case**
    * ["Test", 0, "-14.06.78"]
1. Given an array a of numbers and a target value t, find two numbers that sum to t (that is, a[i] + a[j] = t).
  * **Normal**
    * [2, 8, 11, 7, 12, 0.0e1, -0.123123], target = 7
  * **Unusual**
    * [-2, -2, 8, 7, -7, 8, NaN, +Inf, "0", -0], target = -7
  * **Edge Case**
    * ["Test", 0, "-14.06.78"], target = ''
1. Given a list of n strings with mixed casing, return a new list of all strings that start with a capitalized letter.
  * **Normal**
    * ["test", "AbC", "TeSting", "ABC"]
  * **Unusual**
    * ["tesT", "ABC", "testing", 0, NaN]
  * **Edge Case**
    * ["Test", 0]
1. Find the longest substring of unique letters in a given string of n letters.
  * **Normal**
    * "Very long input"
  * **Unusual**
    * "DSDNjndjsndksandkNJBDjbsjdbsjdbsjbdjB21312312r1njndjsan"
  * **Edge Case**
    * None

## Practice Interview

Interviewer: Timo
Interviewee: Tom  

Challenge:
> Given a list of n strings with mixed casing, return a new list of all strings that start with a capitalized letter.

[] Restate<br>
[x] Question<br>
[x] Assumptions<br>
[x] Think Out Loud<br>

[] Test Input<br>
[] Simplify<br>
[] Diagram<br>
[] Look for pattern<br>
[] Pseudocode<br>
[] Negotiate<br>


# Homework
* Find **2 new** problems on [Exercism](https://exercism.io/) and solve them following the **problem solving strategy** covered in last class to guide your thinking.
* Run your solution code on at least **2 inputs for each type of test case** covered in this class.
* **Commit** your **solution code** and **test cases** to a GitHub repo and add link to the [course tracker](http://make.sc/spd1.01-tracker).
