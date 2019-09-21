## Big O notation: what is it?

### by James Liu

Imagine that you're an avid track and field fan, and you've decided to watch a race in the Olympics. One race is 400m, which is one lap around the track, and the other is 1200m, which is 3 laps around the track. You don't know exactly how long each race will take, because you don't know *the exact speed* the runners are going to be running at. However, you do know that the 400m race will take a shorter amount of time than the 1200m race, because the runners have less distance to run.

This might be an important decision to make if you're short on time, for example, if you were tuning in during the break between classes. If the two races happen at the same time, you probably want to pick the shorter of the two races to watch, since it'll probably finish sooner.

There are similar problems when it comes to programming. For example, in Python, you've probably had to loop through a range of numbers. Specifically, when you're writing a loop, you know that: 
```python
def function_one():
    for i in range(3):
        do_something_with(i)
```

Will probably take a shorter amount of time to run compared to:
```python
def function_two():
    for i in range(10):
        do_something_with(i)
``` 

 As looping through $\{0, 1, 2\}$ is much faster than looping through $\{0, 1, 2, 3, 4, 5, 6, 7, 8, 9\}$, even if you don't know how fast your computer will take to run `do_something_with(i)`.

In this sense, computer code is very similar to watching a race. You can find out how many steps the program has and get a general idea for how long programs will take to run, especially when you compare them. If you knew that `function_one()` and `function_two()` did the exact same thing, you would always pick `function_one()`, since `function_one()` is the program that would take a shorter amount of time to run, even if you don't know *exactly* how much shorter. In addition, when you look at the number of steps a program will take, you can get a sense for how efficient the program is based on how long it's going to take, and make improvements if needed.

In fact, you can relate the number of steps a program takes to the amount of things you're plugging into the program, [and plot it on a graph as a function, which makes comparing the speed of different programs even easier.](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)

![https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/](https://www.geeksforgeeks.org/wp-content/uploads/mypic.png)

From this graph, we can see that the red line with $O(logn)$ is the best program to pick, because it consistently has the shortest running time, despite the amount of items we throw at it.

The function of a relative measurement of running time and efficiency is called the upper bound of a program run time, and it is described with the big O notation, which [Wikipedia states](https://en.wikipedia.org/wiki/Big_O_notation) as: 
> ...a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity

[formally defined as](https://en.wikipedia.org/wiki/Big_O_notation#Formal_definition)

$$f(x) = O(g(x))\;as\;x\rightarrow\infty$$

This is a fancy way of saying the worst-case scenario running time of a program is limited by a certain function as the number of inputs gets very large.

While the thought of an infinitely large input is terrifying, it makes sense when we're comparing and contrasting code, because we want to know how well the code functions *in general*, as opposed to one specific input. In this case, by making the input arbitrarily large, we can shift the focus onto comparing the actual performance function.

In short, Big O notation, or sometimes simply called "big O", despite its scary-sounding math, is in fact a very simple measurement of performance and efficiency. It is a very useful tool to have for reading and writing code, as well as an important step in picking the right code for the job.
