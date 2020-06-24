# Teddy: Automatic Recommendation For Pythonic Idiom Usage


Purit Phan-udom*, Naruedon Wattanakul*,Tattiya Sakulniwat∗, Chaiyong Ragkhitwetsagul∗, Thanwadee Sunetnanta∗, Morakot Choetkiertikul∗,   Raula Gaikovina Kula†

*Faculty of Information and Communication Technology (ICT), Mahidol University

†Nara Institute of Science and Technology (NAIST)

Email: purit.pha,naruedonw,tattiya.sakul}@gmail.com,{chaiyong.rag, thanwadee.sun, morakot.cho}@mahidol.ac.th,raula-k@is.naist.jp


From intro is from iwesep2019 page. not modified yet

## Introduction

Pythonic code is idiomatic code that follows guiding principles and practices within the Python community.
Offering performance and readability benefits, Pythonic code is claimed to be widely adopted by experienced Python developers, but can be a learning curve to novice programmers. 
To aid with Pythonic learning, we create an automated tool, called Teddy, that can help checking the Pythonic idiom usage.
The tool offers a prevention mode with Just-In-Time analysis to recommend the use of Pythonic idiom during code review and a detection mode with historical analysis to run a thorough scan of idiomatic and non-idiomatic code.
In this paper, we first describe our tool and an evaluation of its performance.
Furthermore, we present a case study that demonstrates how to use Teddy in a real-life scenario on an Open Source project.
An evaluation shows that Teddy has high precision for detecting Pythonic idiom and non-Pythonic code. 
Using interactive visualizations, we demonstrate how novice programmers can navigate and identify Pythonic idiom and non-Pythonic code in their projects. 

<figure><iframe width="560" height="315" src="https://www.youtube.com/embed/tmmsqCOxUic" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure>

## Pythonic and Non-pythonic Idiom Database
The dabase can be accessed via this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/python-idioms
Ground truth data that are used to evaluate the configuration of Siamese are in this link: https://github.com/MUICT-SERU/SP2019-08-TEDDY/tree/master/evaluation

## Case Study on Project Flask (https://github.com/pallets/flask)

### Prevention Mode
https://github.com/MUICT-SERU/flask/pull/1
### Detection Mode
https://github.com/MUICT-SERU/icsme20-teddy-tooldemo/blob/master/flask.html

## More Details
The full detail of the project is in this GitHub repository: https://github.com/MUICT-SERU/SP2019-08-TEDDY


