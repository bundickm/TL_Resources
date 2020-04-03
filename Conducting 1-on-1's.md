# Conducting 1-on-1's

## Purpose
1-on-1's are an opportunity to assess a student's knowledge as well as give them actionable feedback to improve. The regularity of 1-on-1's and the feedback you give is the key to their success. They will help you to become familiar with your students and their capabilities, while also allowing you to identify and correct blockers and bad habits early.

## Format
1-on-1's should be conducted Tuesday to Friday. The time you spend will vary with each student and the content, but it is recommended you spend an average of 15 minutes with each student. Since the amount of time you spend with each student will vary, you should leave a bit of a buffer between 1-on-1's if you choose to have students pick their meeting times.

During 1-on-1's you will mainly be reviewing the previous days assignment. This does not mean simply checking that they completed it and asking them if they have any questions. You should be giving feedback on their code, asking them to explain portions they may have copied from lecture or Stack Overflow, and probing their understanding of the concepts with questions not explicitly on the assignment. Constant feedback drives the improvement of their code and it's readability. Having students explain code or concepts helps to develop a deeper and more critical understanding of their work.

For an idea of what to look for when reviewing your students' code, look to the section below. For questions that will help you probe your students' understanding of the concepts, look to the "1-on-1 Discussion" section of each day in this repo. Lastly, if you see a portion of code that looks borrowed from somewhere or just looks particularly interesting, simply ask the student to explain it to you in detail - not just a brief one sentence summary.

## Feedback
Below are various things you should be looking for in addition to simple assignment completion. Students should hear this feedback regularly to reinforce its importance, that means pointing it out when it is incorrect and praising it when it is correct. Finally, don't forget to give the reason why they should listen to your feedback - "because I said so" doesn't work with children and it sure won't work when critiquing code.

For examples from student code, look at [this notebook](https://github.com/bundickm/TL_Resources/blob/master/Misc%20Resources/Compiled_Code_Reviews.ipynb) of compiled code reviews.

### Readability
- Code should be consistent. In Python, like most programming languages, there is more than one way to do anything. Students should be choosing the method that allows for the maximum level of consistency unless they have an explicit reason not to. A common example of this is when referencing columns in a dataframe, switching between dot notation (`df.column`) and square bracket notation (`df['column']`). In this example, square bracket notation should be used since it can always be used where as dot notation breaks down in scenarios such as a space in the column name.
- Use blank lines to break up logical chunks in the code. This makes it easier to "chunk" the code in your mind making it faster to scan.
- Use of functions helps to further label your code and make it easier to read
- Descriptive variable, function, and class names make it clear what's contained in them and also makes code read more like plain English. Students should not be using single letters or obscure abbreviations for names. Example: `x` is bad in most cases, `total` is better - it tells us its purpose, `sum_of_squares` is best in this case - it tells us its purpose and how the value was derived.
- Markdown is used to break up sections and to give context/detail

### Comments
- Comments should generally explain why, not how - if you are using descriptive variable and function names then the how should be clear in most cases
- Comments explaining how should only be reserved for more complex chunks of code
- *Exception*: docstrings in functions and classes

### DRY Code
- Loops, functions, and classes should be used when possible. Look for chunks of code that look like they have been copy and pasted with minor changes such as changing out a column or variable name.
- Functions should be used to do two things, make code repeatable or compartmentalize and label chunks of code. Code structure and flow becomes more apparent than if we had one giant code block. It also becomes trivial to rearrange, add to, or remove code by simply moving the function calls. Finally, corrections are easier, simply go to the function containing that code chunk. Without functions, a change might require editing multiple duplicate points in the code
- Function names should be descriptive, creating self-commenting code
- Functions should be ideally do one thing, if you can describe what they do with "and" its a possible indication to break it into smaller functions. The exception to this idea is a group of functions inside a function, such as a wrangle function that has smaller functions in it for the various feature transformations like handling nulls, handling datetime, etc.

### Markdown
- Markdown should make it easy for someone to read through your work and follow your thought process from start to finish
- Use markdown headers to break up sections of the notebook
- Use markdown text to give detailed explanations of what and why you are doing something. Important things to note include tradeoffs, reasoning, considerations, etc.
- Use markdown to show outside images when needed

### Miscellaneous
- [PEP8 styling](https://www.python.org/dev/peps/pep-0008/) should be enforced from day 1
- Often times students won't know of functions in common libraries, or won't know how to fully utilize them. Look for portions of code that could be simplified with pre-existing tools to save them from reinventing the wheel.


---


[1-on-1's from the TL Handbook](https://www.notion.so/Project-Review-Guidelines-All-Tracks-f15eae123a5645e0ae21f8393c51c866)