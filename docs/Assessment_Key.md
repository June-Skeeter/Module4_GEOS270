---
layout: default
title: Assessment Key
nav_order: 5
parent: potat
---

# Assessment
{: .no_toc }

You can use the course Canvas page to complete the quiz, written submission, and files uploads.  I suggest you download write down your answers as you progress through the Content and Application sections then upload your answers to canvas once you have finished the module.

1. TOC
{:toc}

---

# Module Quiz (25pts)

All quiz answers are multiple choice, numeric input, fill in the blank, etc. type questions.  They can be submitted via the Module 1 Quiz that can be found on the Canvas page.  You will have unlimited attempts to take the quiz.


## Content


[**QC1**](Content.md#qc1)

The [Clip/Intersect/Union] tool can be used to identify the areas of two or more [vector/raster] layers that overlap *and* combine all attributes to create a new layer.

Correct:  **Intersect, vector**

[**QC2**](Content.md#qc2)

The [Clip/Intersect/Union] tool can be used to combine all attributes of two or more [vector/raster] layers and create a new layer.  This tool will include non-overlapping area in the output.

Correct:  **Union, vector**

[**QC3**](Content.md#qc3)

The [Clip/Intersect/Union/Erase] tool can be used like a cookie cutter.  It cuts away the portions of an input that do not overlap the clip layer but does not merge attributes.

Correct:  **Clip**

[**QC4**](Content.md#qc4)

The [Weighted Overlay/Slope/Union/Zonal Statistics] tool can be used to conduct suitability or risk analysis.  Multiple [raster/vector] layers are overlaid to generate a suitability or risk classification map.

Correct:  **IntWeighted Overlay, Raster**


[**QC5**](Content.md#qc5)

The [Raster Calculator/Weighted Overlay/Union/Zonal Statistics] tool can also be used to conduct suitability or risk analysis, but it is a more general tool that allows you to define algebraic expressions using raster layers.

Correct:  **Raster Calculator**

[**QC6**](Content.md#qc6)

The [Slope/Aspect/Reclassify] tool can also be used to calculate the compass direction that a hillside is facing.

Correct:  **Aspect**

[**QC7**](Content.md#qc7)

Stratified random sampling is a(n) [biased/unbiased] sampling method that seeks to draw a more representative sample than pure random sampling.

Correct:  **biased**

[**QC8**](Content.md#qc8)

Spatial [autocorrelation/interpolation/overlay] effects the results we get when sampling spatial data. It is important to think through the impacts when we are sampling spatial data.

Correct:  **autocorrelation**

[**QC9**](Content.md#qc9)

Spatial [Interpolation/Overlay/Sampling] is a process used to "read between the lines" or infer what values are between locations where we have measurements.

Correct:  **Interpolation**

[**C10**](QContent.md#qc0)

Our guest speaker Alysha is the ______ for Peace Geeks, a non-profit that builds digital tools that provide refugees and immigrants crucial knowledge to take charge of their migration journeys.  Peace Geeks developed an app called ______ to help newcomers to British Columbia and Manitoba find information and connect with free services.

Correct:  **Product Manager, Peace Geeks**


---

## Application 

[**QA1**](Application_Part1.md#qa1)

The maximum wave height recorded at Tofino was only ____ meters.  Despite this, wave heights exceeded 8 meters in Port Alberni.  

2.4

[**QA2**](Application_Part2.md#qa2)

Why do we use a feature dataset to hold all our input layers?

* No reason
* So everything is neatly grouped in one folder
* To ensure all our vector data is in the same projection, the feature dataset will automatically re-project our vector data when importing
* To ensure all our vector and raster data is in the same projection, the feature dataset will automatically re-project our vector and raster data when importing

C

[**QA3**](Application_Part3.md#qa3)


Why are we using model builder for this analysis?  Select all that apply

* Your analysis is easily repeatable when using model builder
* You can share your easily update your analysis
* You can share your visualize your workflow
* You can share your workflow

All


[**QA4**](Application_Part3.md#qa4)

How many **km** of roads are at risk?  Rounded to the nearest tenth km is fine.  *Hint* Open the attribute, of PA_Roads_Flood, click right Click Shape_Length >> Statistics to find the sum.

49.6 km


[**QA5**](Application_Part3.md#qa5)

How many residential properties (single and multi-family combined) are are at risk?  

689

[**QA6**](Application_Part3.md#qa6)

What is our estimate of Pop_at_Risk?

1444

**Wrong**: 1443.9 - you can't have nine tenths of a person


[**QA7**](Application_Part4.md#qa7)

How many **km** of roadways are at risk of flooding?Rounded to the nearest tenth km is fine.  

70.6
Correct:  **70.5 - 70.7**
Half Pts:  **69.6 - 71.6**

[**QA8**](Application_Part4.md#qa8)

How many properties (of any kind) are at risk of flooding?

1413

[**QA9**](Application_Part4.md#qa9)

How many people are potentially at risk of displacement?

2038

**Wrong**: 2037.9 - you can't have nine tenths of a person

[**QA10**](Application_Part4.md#qa10)

How many shelters are in suitable locations?

2

---

# Module Assignment (70pts)

All written answers should be numbered and record in one document, saved as a .pdf, and uploaded to canvas.  The file submissions should also be saved as .pdf and uploaded as a separate document.  **Written answers can be as brief as you want as long as they answer the question.**


## Content

No written questions for lecture content this module.

---

## Application (40pts)

[**WA1**](Application_Part1.md#wa1) - 10pts

What does the example presented in Ludwin et al. 2005 say about the value that the sciences have historically attributed to traditional knowledge in when it comes to understanding our world? 

The sciences have tended to have a bias against and non-white/colonial/male knowledge and sources.  This is a serious issue, its related to belief perseverance, which we discussed at the beginning of term, and is rooted in white supremacy.  

[**WA2**](Application_Part1.md#wa2) - 5pts

Look back at Ludwin et al. 2005, specifically at the story of Pachena Bay (bottom pg 142 to top of pg 143).  You can find a [full transcription here](https://pnsn.org/outreach/native-american-stories/other-stories/the-tsunami-at-anaqtl-a-or-pachena-bay).  Find Pachena Bay on google maps.  Where is it relative to Port Alberni?  What can you infer from this story about how a megathrust earthquake occurring just off of the coast of Vancouver Island would impact Port Alberni? 

The whole village was destroyed.  Only people living up high on the hill survived.  The bay has a shorter but similar shape to the alberni inlet.  An equivalent earthquake would be VERY bad given the historical evidence.

[**WA3**](Application_Part5.md#wa3) - 20pts


Write a brief (1 page) report for the City of Port Alberin.  The report needs explicity answer the four questions questions:

**1**{: .label .label-red } Which roads are at risk of flooding or damage?

**2**{: .label .label-red } Which properties in the city are at risk?

**3**{: .label .label-red } How many people in Port Alberni are potentially living in areas at risk?

**4**{: .label .label-red } Are the Tsunami Shelters sufficient?


You should briefly summarize the analysis steps you used to conduct the Tsunami Risk Assessment and explain your findings referring to your charts, map, statistics where necessary.

Needs to explain results & answer each question (see above^) (10 pts - 2 each) + introduction/summary of problem (5pts) + explain steps (5pts).  They should make specific references to their results (quote statistics, reference maps), also reference model when discussing the analysis steps.  You don't have to check to make sure their number are "exact" - as that is in the quiz above ^^ but anything they say should be generally correct (eg. if they say all shelters are acceptable, take off pts.)

---

## File Submissions (35 pts)


[**FA1**](Application_Part5.md#fa1) - 5pts

Upload your model to canvas.

Model should have the proper steps (see example Module5_Model.pdf)


[**FA2**](Application_Part5.md#fa2) - 10pts

Upload your Charts to canvas.

Bar charts should show:

1) Total count of properties at risk by ZoneName
2) Population at risk (Pop_at_Risk) by Dissemination Area (spatial_id).

- Be appropriately labeled and styled

[**FA3**](Application_Part5.md#fa3) - 20pts

Upload your Map to canvas.

Map must show: Inundation Zone, roads at risk of flooding, properties at risk, and approved shelter locations (they should either show only the two acceptable shelters, or show the third shelter as a separate class, distinguishing it as unacceptable.)  Use the Symbology to emphasize the Arterial Roads, distinguish between residential and non-residential properties that are at risk, and show the shelter locations with graduated symbols (by capacity).  

- Should be appropriately styled (accessible colors (no red-green color schemes for features that need to be distinguished))


# Rubric 

All written answers submissions will be scored using this generic rubric.  Your TA will provide brief comments where applicable.  For more feedback you can follow up with your TA.

|Score|Comments            |
|-----|--------------------|
| 0%  |Missing             |
| 25% |Insufficient        |
| 50% |Below Expectations  |
| 75% |Met Expectations    |
| 100%|Exceeds Expectations|
