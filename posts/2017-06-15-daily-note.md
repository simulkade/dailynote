<!-- 
.. title: 2017-06-15 daily note
.. slug: 2017-06-15-daily-note
.. date: 2017-06-15 09:03:47 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

1- Do we pay enough attention to the boundary conditions? Sometimes too much, sometimes too little. I have read many papers, that simulates a physical system, that is well described, with no mention of the boundary conditions. Consider [Danckwerts](https://en.wikipedia.org/wiki/Peter_Danckwerts) [boundary condition[(http://www.sciencedirect.com/science/article/pii/0009250953800011). Many people don't consider it in their simulations. Wrong boundary conditions results in erroneous outcome from a well thought-out model. I'm going to consider the importance of the boundary conditions in my reviews; major revision if you fail to describe it! When do we pay too much attention to the boundary conditions? Mostly in life, specially in politics. I have to think more about it.  

2- Write a post about the change of temperature with altitude in the atmosphere. Use coolprop.  

3- This is how I read excel files (different sheets) and save the sheets as csv files using Pandas, PyCall, and Julia.

```julia
# make sure that pandas and xlrd are installed:
# sudo pip install pandas
# sudo pip install xlrd
using PyCall
@pyimport pandas as pd
file_names=["Geothermal_Q100_.xlsx", "Geothermal_Q150_.xlsx", 
    "Geothermal_Q200_.xlsx", "Geothermal_Q250_.xlsx"]
for fn in file_names
    x1=pd.ExcelFile(fn)
    sh_names = x1[:sheet_names]
    for sh in sh_names
        df = pd.read_excel(fn, sh)
        df[:to_csv](fn[1:end-5]*sh*".csv")
    end
end
```

4- Finally finished the code for the geothermal energy problem, including the sensitivity analysis. I'll run it on my other laptop at home. This laptop is fine, but not a workhorse. The outcome of these simulations will be in a paper, and most probably in a presentation next month.  

5- A quiet evening. Birds chirping outside the window and I'm killing myself by listening to [this song](https://www.radiojavan.com/mp3s/album/Homayoun-Shajarian-Rage-Khab?index=0) from Homayoon Shajarian. What an amazing voice. The results of my simulations are good. So far I have only analyzed a few samples, and now I'm going to do all 150 simulation results automatically. You can find the results of my work in [this repository](https://github.com/simulkade/geothermal).  
