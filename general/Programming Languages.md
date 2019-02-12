## Interpreted Languages
Interpreted programming languages are usually the easiest to learn. The idea is that the computer is able to keep track of the state of your code, line-by-line, on the fly. This allows things like interactive shells that you can type code into and run in real time. Generally, new programmers learn an interpreted language before a compiled language, because the learning curve to make something useful isn't very steep.

As you make a decision about what to spend your time learning, keep in mind one very important thing: **don't try to learn them all**. Interpreted languages are handy, but with few exceptions they perform more-or-less the same functions, and quite slowly. As a new programmer, pick whichever one sounds the most interesting to you, learn it front to back, and move on to a compiled language.

### Python
Link: https://www.python.org

I personally love using Python day-to-day. Writing it almost feels like telling the computer in English what to do. Of the many interpreted languages out there, Python is the one the development community chooses time and time again. Third-party libraries with [pip](https://pypi.org/) and [conda](https://conda.io/en/latest/) are expansive, and there's pretty much nothing you can't do if you're good with Python.

#### Benefits
- **Python is object-oriented**. Learning Python first puts you in a good position to learn most of the common compiled languages like C++, C#, Java, and Rust.
- **Python is great for data analysis**. With tools like [numpy](http://www.numpy.org/), [scipy](https://www.scipy.org/), and [matplotlib](https://matplotlib.org/), doing exploratory data analysis and statistical modeling is easy in Python.
- **Python is the tool of choice for big data**. There are mountains of tools for doing big data analysis, some of the most popular including [HDFS](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html), [BigQuery](https://cloud.google.com/bigquery/), and [Spark](https://spark.apache.org/). All of these tools have Python APIs, as the community as a whole has decided to make it the language of choice.
- **Python has first-class AI tooling**. Given the popularity of Python as a tool for big data, big companies like Google and Facebook have released top-tier machine learning tools - [TensorFlow](https://www.tensorflow.org/) and [PyTorch](https://pytorch.org/) just to name a couple.
- **There are tons of tools to make Python faster**. JIT compilers are becoming very popular. If you have some intensive code that uses numpy, [numba](http://numba.pydata.org/) can probably make your code run an order of magnitude faster.
- **If you need more speed, write in C/C++ then port to Python**. Since Python is written in C, the authors made it easy to [write some C or C++ and port it into Python](https://docs.python.org/3/extending/extending.html). If you're hitting a speed bottleneck in your Python code, you can always write it in a compiled language and port it into your Python script.
- **Python is popular for web development**. [Flask](http://flask.pocoo.org/) and [Django](https://www.djangoproject.com/) are two very popular web frameworks, built with Python. While they aren't as capable as large frameworks like Angular and React, they do make running simple websites quick and easy.
- **Python jobs are in demand**. In a [Stack Overflow survey from 2018](https://insights.stackoverflow.com/survey/2018/#technology-programming-scripting-and-markup-languages), Python was ranked just behind JavaScript as the most in-demand interpreted language.

#### Drawbacks
- **Python has two different versions that the community uses**. Python 2.x and 3.x are incompatible, yet even though 3.x is more efficient and came out many years ago, the world seems reluctant to move off of 2.x.
- **Base Python is not fast**. Depending on the benchmark you use, Python runs anywhere form 50-200 times slower than pure C or C++. *This is true of nearly all interpreted languages, and is not specific to Python.*
- **Python is dynamically typed**. Staticly typed variables are more efficient for the computer to work with in memory, and by default Python does not support it. *I should mention that starting with Python 3.5, [static typing is included](https://docs.python.org/3/library/typing.html) as an optional add-on.*

### R
Link: https://www.r-project.org/

#### Benefits

#### Drawbacks


## Compiled Languages

### C++
Link: http://www.cplusplus.com/

#### Benefits

#### Drawbacks

### C#
Link: https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/

#### Benefits

#### Drawbacks


## Web Frameworks

### Angular
Link: https://www.angular.io/

#### Benefits

#### Drawbacks

### React
Link: https://www.reactjs.org/

#### Benefits

#### Drawbacks
