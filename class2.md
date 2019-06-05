# SPD Class 2 Communication (Part 1)

### Communication-focused steps of the technical interviewing process:
1. Restate the problem
1. Ask clarifying questions
1. State your assumptions
1. Think out loud
  * Brainstorm solutions
  * Explain your rationale
  * Discuss tradeoffs
  * Suggest improvements

### Alan interviewed over 300 people
* He wrote this class plan.
  * Very detailed curriculum.
* Colleges usually don't teach this.

# Interview Process Skills
> "Write a function that takes two lists named a and b, and returns a list of common values that are in both lists."

## Restating the problem in your own words helps ensure:
1. You heard the interviewer’s words correctly and didn’t miss anything
1. You interpreted the interviewer’s words as they intended
1. You’re able to articulate the problem in a way that makes sense to you
  * Do not simply repeat back the exact same words the interviewer just said or wrote down. It’s important to restate the problem in your own words to confirm your understanding.
1. You understand what the inputs and outputs are
1. You’re able to relate the problem to similar ideas

> If you didn’t even understand the problem correctly, you won’t be able to solve it correctly

## Challenge: Restate the problem in your own words
> So we take two lists as input and have to output a list with only the values that can be found in both lists even if at different indexes in their individual lists. - Timo <br>

> So you want me to define a function with two parameters, a and b. Oh, the inputs are lists! And I need to find all the elements that are in both of the lists. Do I print them out…? No, wait! I think you said return a list with those elements. Is that right? `Is that the problem you asked me to solve?` - Alan

* It has to sound human.
* `Rearranged` the question.
* Mention tests (good way to start interview).
* You can add a "is this what you meant?"
* Once you understood what it means, try to ask clarifying questions.
* The vast majority of the time, an interviewer will leave out some innformation and won't be perfectly detailed.
* Asking good clarifying questions make you look better.
  * `What happens when there's duplicates within the same list? Do I add it twice to the output list?`
  * `What if the list is empty?`
  * `Does sorting of the list matter?`
* You can't use libraries that solves the problem in one line.
  * `I guess I can't use the built in functions that solve it in one line..`

## In pairs, create clarifying questions
> Do the lists contain objects of the same type? <br>
> Are the lists sorted? <br>
> Do we know how long the lists are?

### Examples of great clarifying questions:
* Are the numbers integers or floats? Could the numbers be negative?
* Could the input contain duplicates? Should I include only one of them?
* What if I find the same string with different casing, is that the same word?
* Is the input array already sorted? Can I modify the input parameters?
* Should I find all solutions or just the first? What if there’s no solution?
* What type and value should the function return? Does the order matter?
* Is it OK to use the built-in ___ function/class? Can I use the ___ library?

* What `types` of lists are the two inputs? Are they arrays or linked lists?
* Are the input lists always `small` or could they sometimes be really `large`?
* What types of values are in the input lists? Numbers? Strings? Objects?
* Could either of the input lists contain `duplicate` values? If so, should I include that value in the output list `multiple times` or only once?
* Are the values in the input lists in `sorted order` or `arbitrary order`?
* Can I `modify` either of the input lists? Or do I need to leave them as-is?
* Should I return a `new list` as output? Does the `order of` the values matter?
* Is it OK to use the built-in `sort` function? What about the `set` class?

# Stating Assumptions
## Common assumptions:
* Numbers are integers / positive
* Input is unsorted (arbitrary order)
* Cannot modify input parameters
* Create new structure as output
* Order of output does not matter (unless otherwise stated)
* Can use built-ins (unless it makes solution only one line of code)

### Benefits:
* Demonstrates good judgement for designing new components
* Simplifies problem to produce a solution for simple/common case
* Risks of not listing assumptions:
* Get stuck trying to solve hardest version of problem and not finish

> Interviewer thinks: “This person can make reasonable assumptions to simplify the problem. Very thoughtful.”

> The biggest mistake is making an assumptions before asking it first.

### Writing Assumptions
Alan's:
* I’m going to assume the `types` of the two input lists are dynamic arrays and do not contain any `duplicates` but their values are in `arbitrary order`.
* To make things easier for now, I’ll assume the lists only contain integers, floats, or strings, since those data `types` are `comparable` and `hashable`. Then I’ll check if my solution works on values that are any type of object.
* I think you meant that I should return a `new list` as output that does not contain `duplicate` values and the `order` of the values does not matter.
* I’m assuming if the function is given the `edge case` where the two input lists have no common elements then the `output` should be an empty list.

# Think Out Loud
> You don't have to state everything you think of, just keep the following on your train of thoughts.

> If you go quiet for more than 20 seconds, you will concern the interviewer on your capabilities.

> It is possible to over-talk, you might seem nervous or will not catch some crucial hints.

### Alan gave us a out loud thought example
* He iterated over his idea many times.
* He was giving a performance analisys while thinking of ideas.
* Try not to look unconfident.
* But try to say `I think...`

## Brainstorm Solutions
> Brainstorm several different ways you could approach the problem by trying to solve it as a human.

You should **NOT** write any code (or even pseudocode), you’re just coming up with lots of different ideas, organizing your thoughts, and thinking out loud about how you would approach the problem.

#### Do:
* Walk through the problem by hand, using a small example input (e.g., array of 3 or 4 elements) or a data structure diagram (e.g., linked list of 3 nodes that you can reverse manually)
* Create a list of solution ideas with keywords to remind you (e.g., “sort array => binary search”)
* Name a few common data structures and see if you could apply any of them to the problem

#### Don’t:
* Get stuck on one idea for too long – the goal is to generate a list of several solution ideas
* Get into the implementation details of a solution – remember, this is the brainstorming step!
* Stay quiet and wait for the perfect solution to strike you like lightning from the gods of coding

## Explain Your Rationale
Explain the rationale of your solution to justify your choices and demonstrate your understanding of programming and computer science concepts.

#### Qualities of effective rationalization:
* Explains why you chose to use a certain operation or data structure
* Connects to design constraints in the problem or assumptions you made
* Mentions performance considerations (i.e., time and/or space complexity)

#### Examples of effective rationalization:
* “I want to sort the array so that I can use binary search to find a value.”
* “I’ll use a hash table because I can look up a value by key very quickly.”
* “Using a set makes sense because we don’t want duplicate elements.”

## Discuss tradeoffs
Explain the tradeoffs (i.e., pros and cons) to your solution, as well as how it compares to other solution ideas you generated in the brainstorming phase.

#### Examples of effective tradeoff statements:
* “This is a naive solution, so it’s quick and easy to code and doesn’t use any extra memory, but its time complexity is O(n2), which is fairly slow.”
* “This is better than my first solution because it only takes O(n log n) time.”
* “This solution runs in O(n) time, which is really fast because a set uses a hash table for fast lookup but it takes O(n) extra memory and the output is in arbitrary order. Oh, and it also requires all input values to be hashable.”

## Suggest Improvements
Analyze the weaknesses (e.g., limitations or performance bottlenecks) in your solution and generate new ideas to discuss how you could improve upon it.

If you have enough time, change your code to include this improved solution.

#### Examples of analysis and suggested improvement:
* “My solution takes O(n2) time, which is pretty slow, since it has a nested for loop. I need that because I’m searching the list for the other element. Oh, wait! Maybe I could search faster if I sort the list or instead use a set!”
* “This solution is really fast, but it only works for numbers. I think I could also make it work for strings, but I’d have to change this part right here.”

# In Class Activity
With a partner, follow the notes and solve the solution. Once you're done, let them do the same.

Best Solutions:
1. `O(n)` Set and intersect function.
2. `n * log(n)` First loop on one list, sort the second and run binary search.
3. `O(n)^2` loop over both.

# Homework
* Worksheet ([link](https://docs.google.com/document/d/1eW9jdLTXpWN2eNhkncqfcddDri1jQvW2W1zIYlFsq68/edit))
  1. Fill out the worksheet by yourself
  1. Compare your answers with a partner
  1. Class views completed worksheet
* Partner Assignment
  * Find a partner and choose one of the below problems. You will go through the problem as if you were in an actual interview. Your partner will  play the interviewer, and will have a checklist to make sure you’re following the proper steps
  * Swap roles and pick a different problem
  * Repeat twice with a new partner for questions 3 and 4
  * **Problems:**
    * Fibonacci
    * FizzBuzz
    * Factorial
    * Duplicate value
