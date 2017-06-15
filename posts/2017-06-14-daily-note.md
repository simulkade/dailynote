<!-- 
.. title: 2017-06-14 daily note
.. slug: 2017-06-14-daily-note
.. date: 2017-06-14 08:54:43 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

1- I just learned [a good trick](https://askubuntu.com/questions/490612/how-do-i-automate-the-activation-of-python-environment#comment656705_490613) to start my python 3 virtual environment that I use for running Nikola to update this blog. Add the following line to the end of your .bashrc file (located in your home folder):

```
alias py3="source ~/(path to your virtualenv)/bin/activate"
```

Now I can easily start my virtual environment by typing `py3` in the terminal.  

2- I just found out that in my `JFVM.jl` package, I can create 2D and 3D cell variable by assigning 1D arrays of the right size to the `createCellVariable` function, without reshaping the 1D array! It makes things (just a bit) easier in my reactive transport codes.  

3- I bought some dried fruits and cashew nuts from [this online shop](https://www.basboernoten.nl). I just want to recommend it here if you happen to be close to the Netherlands. They have excellent products with a reasonable price (for this region).

4- Finally solved the geothermal problem in Julia, and just in time, because I have to go and pick up Aida from school.
