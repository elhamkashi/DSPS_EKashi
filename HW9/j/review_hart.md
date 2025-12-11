Task 1 Review:
Initial Plot
![Project Logo]((https://raw.githubusercontent.com/elhamkashi/DSPS_EKashi/main/HW9/j/original%20bad%20plot.png))


Visualization:

In terms of ambiguitity, the labels are too crowded together and large to be able to actually make anything intelligible out here. The image itself also isn't zoomed in enough, or there are too many
variables considered, meaning that the indiviudal relationships between the variables isn't conveyed well at all. 

I don't think that the plot is too distorted. It is really difficult to actually get any real useful information from the scatter matrix, but I don't think it is inentionally misleading. 

The scale of the labels is very distracting. They are too large and overlap a lot, becoming completely unreadable, as well as just generally distracting. 



Tufte's Rules:

Effect Size: Once again, I think the numbers are too large here and the relationship plots are too small, so those parts of the data are being misrepresented.

Data/Ink Ratio: The labeling is not clear and actually makes it harder to understand the point of the plot.

Redundancy: The scatter matrix does show redundant data. The relationships plotted above and below the central diagonal are the same. 


Remade Plots:

![Project Logo](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/j/Task1/Clustered%20correlation%20matrix.png?raw=true)


![Project Logo](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/j/Task1/Masked%20correlation%20matrix.png?raw=true)

I think that the switch to a correlation heatmap is very effective here and solves one of the major problems of the original plot. 
In the first plot, the individual relationship subplots couldn't be interpreted because they were too small. Rather than removing data to zoom in,
the heatmap quantifies how related certain variables are with color. I think that is a very good way to make the plot less ambigious and distorted. 

The dendrograms help to make the labels less ambigious and distracting by showing the relationships between variables in an easier to read way.

The second plot is also way less redundant because it cuts out the duplicated variables. It also keeps the labels a similar size, but removes
a lot of them to make it easier to read (only covering a few intervals).

The color map on the sides of the plots also provide the necessary information to understand the figure. 

The data/ink ratio is much better here especially because of the removed labels. 

The color scale going from red to blue does well to represent continuous information like the relationships between variables displayed here. It is also unlikely to cause
confusion due to color blindness.




Task 2 Review:


![Project Logo](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/j/alp-bad.png?raw=true)

This figure has a lot of information, but a lot of it could not be interpreted by just looking at the plot and reading the labels.
I would not have been able to figure out what the dashed and solid lines represent here had I not read the description. 
I think the axis are well labeled and show a good data/ink ratio. I also think that the theoretical regions are labeled and conveyed well


The plot contains some abiguity with the crowding of labels and lines near the center of the plot. I think labels like the transparency hint and stellar cooling hint can lead to confusion
about what they are referring to. 

I actually think that the colored labels that correspond to different limits and predictions helps to reduce possible distractions quite a lot. 

There are a lot of labels for different points in the limits and predictions that may not be necessary. The chart probably uses too much ink relative to the information
it is trying to convey and has some 'junk' elements. 



![Project Logo](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/j/axionphoton-good.png?raw=true)

The more consistent color scheme for this plot helps to make it less distracting. For me, the blue labels seem to be a little ambigiuous as to what they represent. 
There are a lot of dashed blue lines corresponding to these labels, but they overlap and are confusing, so I think that element is still flawed here. 
Other lables like the GC Magnetar are pretty ambigiuous. 

This plot does simplify and reduce some of the clutter of the previous plot while representing the same information. I think it obeys Tufte's Rules better as the effect
size is consistent. Most elements are labeled, so the data/ink ratio is good. I do think that this figure still struggles with chart junk and it may actually be more 
confusing than the first in certain parts. The removal of the theoretical region color-coded labels does make it simpler and more intelligble though. 

The colors do help keep the different regions distinct. I think the color choice could cause some confusion with some types of color blindness (protanopia) with the use 
of yellow and green. 
