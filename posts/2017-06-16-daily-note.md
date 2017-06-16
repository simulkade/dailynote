<!-- 
.. title: 2017-06-16 daily note
.. slug: 2017-06-16-daily-note
.. date: 2017-06-16 08:26:26 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

1- Last night, I managed to analyze all my simulation results in with a short Julia script. The visualization looks quite good. Today, I'm going to do the difficult part: describing and discussion the results. I'm probably going to stick to my own simulation results, which is more comprehensive in terms of analyzing the effect of various parameters.  

2- This is the first paper that I'm writing using my finite volume toolbox. The number of users of this tool has grown since I published it online, and several researchers asked me how to cite it. Perhaps, it is the time to think about a publication. I know a couple of educational journals, but they are not openly accessible. I will look around for a publication. Perhaps I can write a paper and ask a couple of friends to review it and then get a doi for it from Zenodo. It can be uploaded on the same repository, including the reviews. I go for the latter.  

3- I have helped many colleagues and students during my life, and many have helped me. During a discussion, my former supervisor pointed out that it is nice to help others, but I should not be very idealistic about it. It is important that my help (that can easily lead to a considerable contribution) is acknowledged in one form or another, e.g., being mentioned in the acknowledgment section of the thesis or paper, or even better by co-authorship. This is something I have practiced myself. Usually, my acknowledgment slide is not at the end of the presentation but right at the beginning. Sadly, not everybody practices this unless they are told or even coerced to do so. The reason I wrote this is that I just saw a publication from a student, whom I helped a lot. I even shared some of my unpublished codes with him. Of course he thanked me verbally, but when I look at the list of the authors on his paper, I can see that my contribution has been way more than one or two co-authors. I'm not unhappy about it; but I care enough to write about it here.  

4- My brain is blocked again. The simulation results are analyzed. There are a lot of things that I can describe, yet I do not know how to start. Let's write my thoughts here.  
I rewrote the whole model in my own FVM code, because I wanted to have more simulation results. I also was thinking about making the model more accessible by using a free software (in this case my own JFVM.jl). Previously, we had only 25 simulation results. Now it's 150. I'm looking into some important factors:
  + Project life time: when cold water breaks through the production well, the project is done. The production stops until the earth warms up the cold water. I have calculated it in my simulations. 
  + CO2 emission per unit exergy: from a societal point of view, it is important to have an exergy source with the lowest CO2 emission. Usually, I compare this factor with the CO2 emission of methane, that has the lowest CO2 emission among the fossil fuels (roughly 0.05 kg/MJ exergy]. Here, I'm looking only at the exergy value which is somehow not fair, since I have calculated it from the exergy of the produced hot water. I cannot really warm up the same amount of water by burning methane. Perhaps, it is necessary to consider the energy content as well (possible to do in my analysis code).
  + Recovery factors: this is the outcome of my PhD thesis; the extracted resource must be able to pay for the extraction and clean up processes, otherwise the whole process is not practical. This is a clear concept but does not consider the scope. It can be addresses by only analyzing the a range of realistic process parameters, e.g., not a very low production rate.  

5- I did the new calculations and created the table of results. I think the story looks better now. I have a process, that consumes some fossil fuel and delivers some heat. This process can be a direct combustion of the fossil fuel or conversion of the fossil fuel to electricity to drive a geothermal circulation pump or a heat pump. Now we are going to compare them.
