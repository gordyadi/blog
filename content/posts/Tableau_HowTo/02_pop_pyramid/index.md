---
title: "Animated Population Pyramid"
date: 2021-02-09
description: Singapore's population pyramid from 1980 t0 2019
menu:
  sidebar:
    name: Population Pyramid
    identifier: Population Pyramid
    parent: Tableau How to
    weight: 100
math: true
---

---

*Documenting my Tableau learning journey.*

---

## Population Pyramid

Click play to see how Singapore's population changes across the years.
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/popchart.gif" align="left" >}}  
Full visualisation available on [Tableau Public](https://public.tableau.com/profile/suyiinang#!/vizhome/Singaporespopulationpyramid/Dashboard1).  


## Good for
Analysing population by age and gender.

## How to create - step by step
**The data**  
I have used the Singapore Residents By Age Group, Ethnic Group and Gender from [data.gov.sg](https://data.gov.sg/dataset/resident-population-by-ethnicity-gender-and-age-group?view_id=8ff89d3f-48c8-46e4-8a4d-a8b9f152976f&resource_id=f9dbfc75-a2dc-42af-9f50-425e4107ae84).  

Before loading into Tableau, I have extracted only the female and males data from 1981 to 2019 using Excel as the remaining data is irrelevant for this exercise.  

**Step 1 - Data in correct data type and rename headers**   
I have made the necessary changes to the data types and renamed headers to the following:  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig1.png" align="left" >}}

**Step 2 - Create calculated field for female and male population**  
In order to create a population pyramid, the female and male population needs to be two separate fields.  
To separate them, I created two calculated fields:
1) Male Population  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig3.png" align="left" >}}

2) Female Population  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig2.png" align="left" >}}

**Step 3 - Filter Year**  
Drag "Year" to the Filters Panel and select the year you want.  

**Step 4 - Populate columns and rows**   
Populate rows according to the figure below.  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig4.png" align="left" >}}

**Step 5 - Reverse the male pop axis**  
Right click the x-axis of male population > Edit Axis > Tick "Reversed" under Scale.  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig5.png" align="left" >}}

**Step 6 - Format colour**
Under the Marks panel > Female population > colour > select pink.  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig6.png" align="left" >}}

**Step 7 - Name title**  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig7.png" align="left" >}}

You now have a static population pyramid chart!  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig10.png" align="left" >}}

# Now let's add some animation.

**Step 7 - animation**
Remove the "Year" from the Filters panel and drag "Year" to the Pages panel.
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig8.png" align="left" >}}
This slider should show up to the right of your chart:  
{{< img src="/posts/Tableau_Howto/02_pop_pyramid/images/fig9.png" align="left" >}}
Click play to view animation.  

# And... there have you it! An animated population pyramid is ready for analysis!  

---
I would like to thank Prof Kam of Singapore Management University for the inspiration.