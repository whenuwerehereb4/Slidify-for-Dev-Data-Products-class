---
title       : "3d Shiny Plot with Prediction Plane"
subtitle    : "Dev Data Products Project"
author      : "Andrew Nix"
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
<style>
em {
  font-style: italic
}
</style>

<style>
strong {
  font-weight: bold;
}
</style>

## Overview of Plot Contents
This 3-d plot is intended to illustrate the predictions associated with the linear regression model, created from the **mtcars** data set, that predicts miles per gallon (mpg) using the predictors weight (wt) and 1/4 mile times  (qsec).  The plot also includes the individual data points that were used to generate the model.


### **model_final01<-lm(mpg ~wt + qsec,data=mtcars)**


**NOTE:** *Github repo containing the app development files (i.e. server.R, ui.R, global.R and the "Getting Started" content file):*  


https://github.com/whenuwerehereb4/Developing-Data-Products-Final-Project

--- 

## Plot Variables Overview
The plot consists of 3 main variables, corresponding to the x, y and z axes of the plot (which variable corresponds to which axis is interchangeable, but for current purposes we are assuming the z axis refers to the response variable, mpg).   There are 2 secondary variables (outside the scope of the model, itself) that are also built into the plot display, providing additional context and insight.

## Variables Associated with the Data Points

**Prediction Variables**  
1) *Weight (wt)* 
2) *1/4 mile times (qsec)*

**Response Variable**  
3) *Miles per gallon (mpg)*

**Additional variables associated with the Data Points**  
4) *Transmission Type (am)* 
5) *Make Model of Vehicle*

---

## User Inputs and Interaction with the plot 
- **the user can choose to view the plot *with* a prediction plane or *without* a prediction plane**
- the user can rotate the perspective of the 3-d plot by clicking and dragging the plot in any direction of interest. (Just play around with it and get a feel for it)
- the user can provide "inputs" to the interactive 3-d plot by simply hovering over individual data points or areas of the prediction plane.
- when the user hovers over individual data points from the plot, a pop-up text box will appear with the following information:  

*1) the numeric values corresponding to the x,y and z axes described above (x=weight, y=qsec, z=mpg);*  
- available for both the individual data points and the prediction plane  

*2) the make/model of the vehicle* 
-  available only for the individual data points 

---

### Here is what the end result will look like (if the user selects the option to include the prediction plane): 


<iframe src="demo.html" style="position:absolute;height:100%;width:100%"></iframe>


