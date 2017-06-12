<!-- 
.. title: 2017-06-12 daily notes
.. slug: 2017-06-12-daily-notes
.. date: 2017-06-12 09:13:52 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

Supervising master students is a challenge. When I was a master student, I defined my project myself, planned it, did all the experiments, and went to my supervisor's office with the outline of the thesis. He was shocked at the beginning, but helped me to give the text a better structure. I am very proud of what I did at the time. Not all the students work like this. Some need constant attention and guidance. I have supervised (am supervising) more than 10 students. One of them was just amazing. Another one was almost fully independent. Two or three needed a minimum level of attention, and the rest needed constant monitoring and help. Now that I think about it, sometimes, students are somewhere between the third and the last group. The problem for someone like me with a temporary appointment is that we need to do as much as possible in the limited time of our contract; therefore, we prefer to work with the first or second group of students. But unfortunately, these students are always snatched by the Professors, who can easily identify (because they teach and we don't) and attract them. I can narrow down my final problem to this: If I need to spend 3 hours to teach a master student to do a task that I can do in less than 3 hours, I prefer to do it myself. This is, sadly, the only solution that matches the circumstances of a post-doc researcher.  

In matplotlib, I can plot negative values on a (semi)logarithmic scale using the following commands:  

```julia
plot(x,y)
xscale("symlog")
```

I run the above commands in Julia. The same can be done in python by importing `matplotlib.pyplot`.  

I'm on my second long Pomodoro break. My sessions was not as productive. I checked emails a couple of times and did not focus on a single task during my 25 minute sessions. The result is that my progress is not impressive, although it is not bad at all. I wrote only two paragraphs, but I managed to do most of the calculations that I wanted to add to the paper. Before picking up Aida and taking her to the last session of Dutch school, I'll focus more on writing the results and discussion. The simulation results are mostly analyzed. I only need to fit it into my story, without making it yet another spam paper.  

I do not like csv files for storing data. They limit the user to tables, which is a form that rarely appears in real life. Moreover, usually that table describe a time series measurement for a physical system with many other parameters that cannot fit into the same table. Recently, I've started using JSON which gives me what I really need. But for this gepthermal paper, I had only CSV file, with long file names that described the properties of each system! I tried to read the file names and do some analysis on the string to extract the required data, but I gave up and did it manually since there was no pattern in the filenames. Fortunately I had only 20 files and it was not really time-consuming (even though I wasted some time trying to do it automatically!).  


