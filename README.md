# Teddy: Automatic Recommendation For Pythonic Idiom Usage


[Purit Phan-udom](purit.pha@gmail.com), [Naruedon Wattanakul](naruedonw@gmail.com), [Tattiya Sakulniwat](tattiya.sakul@gmail.com), [Chaiyong Ragkhitwetsagul∗](https://cragkhit.github.io/), [Thanwadee Sunetnanta∗](http://mucc.mahidol.ac.th/~ittth/), [Morakot Choetkiertikul∗](https://morakot-ch.com/), [Faculty of Information and Communication Technology (ICT), Mahidol University](https://www.ict.mahidol.ac.th/)

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
|              Type              | Code snippets                                                                                                                                                  |
|:------------------------------:|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pythonic<br>dict comprehension | def i1():<br>&nbsp;&nbsp;&nbsp;&nbsp;emails = {user.name: user.email for user in users if user.email}<br><br>def i2():<br>&nbsp;&nbsp;&nbsp;&nbsp;dict_compr = {k: k*\*2 for k in range(10000)}<br><br>def i3():<br>&nbsp;&nbsp;&nbsp;&nbsp;new_dict_comp = {n: n*\*2 for n in numbers if n%2 == 0}<br><br>def i4():<br>&nbsp;&nbsp;&nbsp;&nbsp;dict1 = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5, 'f':6}<br>&nbsp;&nbsp;&nbsp;&nbsp;dict1_tripleCond = {k:v for (k,v) in dict1.items() if v>2 if v%2 == 0 if v%3 == 0}<br>&nbsp;&nbsp;&nbsp;&nbsp;print(dict1_tripleCond)<br><br>def i5():<br>&nbsp;&nbsp;&nbsp;&nbsp;nested_dict = {'first':{'a':1}, 'second':<br>&nbsp;&nbsp;&nbsp;&nbsp;{'b':2}}float_dict = {outer_k: {float(inner_v) for (inner_k, inner_v) in outer_v.items()} for (outer_k, outer_v) in nested_dict.items()}<br>&nbsp;&nbsp;&nbsp;&nbsp;print(float_dict)<br><br>def i6():<br>&nbsp;&nbsp;&nbsp;&nbsp;fahrenheit = {'t1': -30,'t2': -20,'t3': -10,'t4': 0}<br>&nbsp;&nbsp;&nbsp;&nbsp;celsius = {k:(float(5)/9)\*(v-32) for (k,v) in fahrenheit.items()}<br>&nbsp;&nbsp;&nbsp;&nbsp;print(celsius_dict)<br><br>def i7():<br>&nbsp;&nbsp;&nbsp;&nbsp;mcase = {'a':10, 'b': 34, 'A': 7, 'Z':3}<br>&nbsp;&nbsp;&nbsp;&nbsp;mcase_frequency = { k.lower() : mcase.get(k.lower(), 0) + mcase.get(k.upper(), 0) for k in mcase.keys() } |
| Pythonic<br>enumerate          | def i8():<br>for i, x in enumerate(l):<br>        # ...                                                                                    |

The actual database source codes can be accessed via this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/python-idioms

Ground truth data that are used to evaluate the configuration of Siamese are in this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/evaluation

## Case Study on Project Flask (https://github.com/pallets/flask)

### Prevention Mode
https://github.com/MUICT-SERU/flask/pull/1
### Detection Mode
https://github.com/MUICT-SERU/icsme20-teddy-tooldemo/blob/master/flask.html

## More Details
The full detail of the project is in this GitHub repository: https://github.com/MUICT-SERU/SP2019-08-TEDDY


