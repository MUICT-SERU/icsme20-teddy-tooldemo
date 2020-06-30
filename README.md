# Teddy: Automatic Recommendation For Pythonic Idiom Usage


[Purit Phan-udom](mailto:purit.pha@gmail.com), [Naruedon Wattanakul](mailto:naruedonw@gmail.com), [Tattiya Sakulniwat](mailto:tattiya.sakul@gmail.com), [Chaiyong Ragkhitwetsagul∗](https://cragkhit.github.io/), [Thanwadee Sunetnanta∗](http://mucc.mahidol.ac.th/~ittth/), [Morakot Choetkiertikul∗](https://morakot-ch.com/), [Faculty of Information and Communication Technology (ICT), Mahidol University](https://www.ict.mahidol.ac.th/)

[Raula Gaikovina Kula](https://raux.github.io/), [Nara Institute of Science and Technology (NAIST)](https://naist-se.github.io/)

## Introduction

Pythonic code is idiomatic code that follows guiding principles and practices within the Python community.
Offering performance and readability benefits, Pythonic code is claimed to be widely adopted by experienced Python developers, but can be a learning curve to novice programmers. 
To aid with Pythonic learning, we create an automated tool, called Teddy, that can help checking the Pythonic idiom usage.
The tool offers a prevention mode with Just-In-Time analysis to recommend the use of Pythonic idiom during code review and a detection mode with historical analysis to run a thorough scan of idiomatic and non-idiomatic code.
In this paper, we first describe our tool and an evaluation of its performance.
Furthermore, we present a case study that demonstrates how to use Teddy in a real-life scenario on an Open Source project.
An evaluation shows that Teddy has high precision for detecting Pythonic idiom and non-Pythonic code. 
Using interactive visualizations, we demonstrate how novice programmers can navigate and identify Pythonic idiom and non-Pythonic code in their projects. 

<figure><iframe width="600" height="315" src="https://www.youtube.com/embed/tmmsqCOxUic" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure>

## Pythonic and Non-pythonic Idiom Database
### Pythonic Database Set
|              Type              | Description                                              |
|--------------------------------|----------------------------------------------------------|
| Pythonic dict comprehension | Declaration of `dict` variable and assignment of its elements in a single statement |
| Pythonic list comprehension | Declaration of `list` variable and assignment of its elements in a single statement |
| Pythonic enumerate | For-loop iteration using `enumerate` function |
| Pythonic if statement | Using implicit truthfulness for `if` conditional statement |
| Pythonic file reading statement | Using `with open() ... as` to open a file |
| Pythonic set | Using `set` variable type to create a unique collection |
| Pythonic tuple | Unpacking data for multiple assignment at once |
| Pythonic variable swapping | Using tuple to swap values between two or more variables |
| Pythonic string formatting | Concatenation of multiple string formatting statements, use of `.format()` with placeholder(s) in a static string |
| Pythonic code formatting | Proper use of indentation for code blocks and writing one statement per one line |
### Non-Pythonic Database Set
|              Type              | Description                                              |
|--------------------------------|----------------------------------------------------------|
| Non-Pythonic dict comprehension | Separate declaration and for-loop element assignment of a `dict` variable |
| Non-Pythonic list comprehension | Separate declaration and for-loop element assignment of a `list` variable |
| Non-Pythonic enumerate | for-loop iteration without the use of `enumerate` |
| Non-Pythonic if statement | direct comparison of variable with `True`, `False`, or `None` in the conditional statement |
| Non-Pythonic file reading statement | Opening a file without using `with open() as ...` |
| Non-Pythonic set | Using for-loop to create a unique collection of item |
| Non-Pythonic tuple | Explicitly assigning variables with elements in a collection |
| Non-Pythonic variable swapping | Using a `temp` variable to swap values of two variables |
| Non-Pythonic string formatting | Sequence of one string formatting commands per one line, using '+' to concatenate static string and variable(s) together, or using '%' as string variable placeholder |
| Non-Pythonic code formatting | Using ';' to put more than one statement in a single line |

The full database source codes can be accessed via this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/python-idioms

Ground truth data that are used to evaluate the configuration of Siamese are in this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/evaluation
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
## Case Study on Project Flask (https://github.com/pallets/flask)

### Prevention Mode
https://github.com/MUICT-SERU/flask/pull/1
### Detection Mode
https://github.com/MUICT-SERU/icsme20-teddy-tooldemo/blob/master/flask.html

## More Details
The full detail of the project is in this GitHub repository: https://github.com/MUICT-SERU/SP2019-08-TEDDY


