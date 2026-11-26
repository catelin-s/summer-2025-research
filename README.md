Author: Catelin Smith
Date: August 7th, 2025
Subject: STScI / JHU Summer Astronomy REU

This past summer, I worked with Dr. Beth Sargent at STScI to study the composition of dust around 
oxygen-rich AGB stars and S-type stars. AGB stars are cool, evolved stars that contribute a lot
of the dust seen in our universe. They can be classified into three different categories based
on their C/O ratio. If C/O > 1, they are carbon stars and tend to exhibit amorphous carbon,
SiC, and MgS circumstellar dust. If C/O < 1, they are oxygen-rich (o-rich) stars and will have
dust consisting of various silicates and oxides. Finally, if C/O is near unity, they are S-type
stars and can have any of the dust previously mentioned, though they may favor certain grains
depending on if they're closer to being o-rich or c-rich. 

Both oxygen-rich AGB stars and S stars are known to have a 13 um spectral feature, which can
be accompanied by 20, 28, and 32 um features as well as broader 10-11 um features. While the
13 um feature's source is unknown, we believe it to be corundum, one of the polymorphs of
alumina (Al2O3). By studying and modeling these mid-infrared spectral features in a variety 
of o-rich and s-type AGB stars, we aim to prove this to be true and that other polymorphs 
of alumina are present, contributing to the aforementioned peaks at those wavelengths.

In the first few weeks of my internship, I focused on finding ground-based mid-infrared 
spectroscopy through literature searches to expand our data collection. I found 21 OH/IR
stars, 6 red supergiants, and 12 S stars; we chose to focus on the S stars since they
showed the most promising features and had a wider range of wavelengths. 

Then, I pivoted to modeling, which was done in two ways: an optically-thin method and 
radiative transfer modeling. The optically-thin modeling code works by assuming that
the dust shell is optically thin from 5 - 40 um and creates a grid of two temperatures,
a warm and a cold one. Then, using an equation for flux that utilizes the different grain
opacities, the two temperatures, and a blackbody, we create several different models
of our spectrum and select the temperatures that yield the one with the lowest 
reduced chi-squared value (i.e. the model with the best fit). With this method, I modeled
the 12 S stars, the 6 red supergiants, and a few other S stars and o-rich AGB stars that
I found Spitzer or ISO/SWS mid-infrared spectra for. A few stars emerged as displaying
13 um features and possessing some of the other features as well to some degree: Y Lyn,
IRC+60374, WY Cas, and IRC-10411. 

From there, I chose to model these stars using the radiative transfer code DUSTY, which 
is a one-dimensional solution to the radiative transfer equations. DUSTY is unique in
that it is a scalable code, and I mainly modified the external radiation temperature,
the optical thickness, the dust grains present, the grains' abundances, and the dust
temperature. I collected photometry for these stars using the VIZIER database and
created DUSTY models for all of them, with varying degrees of success.

What all of these models showed is that the presence of corundum and other polymorphs
of alumina fit the 13, 20, 28, and 32 um features very well in S stars, and they do 
not all have to exist together. However, since S stars are also known to possess dust
grains common in carbon stars, some of which can fit the longer wavelength features
too, I decided to model some other S stars that may lean carbon-rich but still possess
a few of these features. This is still a work in progress since I have two weeks left
in my internship and I only started DUSTY modeling in general two weeks ago, so I hope
to have this completed in time and to update this document when done. I hope to find
that there are some intrinsic differences between the 20 and 30 um features of o-rich
leaning S stars and c-rich leaning S stars so that the dust grains can be easily
distinguished from each other. However, if that is not the case, then we must consider
if it is possible for both carbon-rich and oxygen-rich dust grains to coexist.

My list of stars is as follows, with the modeling type (or future modeling) put in
parentheses. I plan on updating as many DUSTY models as possible with stellar
photospheres instead of blackbodies to increase accuracy.

- Y Lyn (OTM and DUSTY modeling)
- IRC+60374 (OTM and DUSTY modeling)
- WY Cas (OTM and DUSTY modeling -- in progress)
- IRC-10411 (OTM and DUSTY modeling -- in progress)
- RW And (OTM)
- IRC-10401 (OTM)
- IRC-10450 (OTM)
- IRC+00402 (OTM)
- CSS241 (OTM)
- CSS1055 (OTM)
- CSS1185 (OTM)
- HD35273 (OTM)
- CK Car (OTM)
- AH Sco (OTM)
- V460 Car (OTM)
- V602 Car (OTM)
- KW Sgr (OTM)
- U Her (OTM)
- RX Boo (OTM)
- FI Lyr (OTM)
- X Oph (OTM)
- V376 Aur (OTM)
- CSS553 (OTM)
- CSS1005 (OTM)
- W Hor (OTM)
- SV Peg (OTM)
- AA Cyg (planned DUSTY modeling)
- RZ Sgr (planned DUSTY modeling)
- W Aql (planned DUSTY modeling -- known to have a lot of carbon dust)
- pi Gru (planned DUSTY modeling)


Additionally, I attended a CLOUDY workshop in early August in Lexington, Kentucky. While 
there, my group utilized CLOUDY to study the extended UV emission of Mira, an oxygen-rich 
AGB star. In 2007, it was discovered that Mira had a bow shock and tail emitted in the UV 
range; this was hypothesized to be due to H2 excitation as the warm post-shock tail gas 
interacted with the interstellar medium. For this project, I completed DUSTY models of both
Mira (o Cet) and R Hya, another oxygen-rich AGB that was later found to have extended UV
emission, in order to gain insight into the stars and create data to compare our outputs
to. To learn more about CLOUDY, I also attempted to model the bow shock of Mira, but I did
not have enough time to complete this due to the extensive nature of that model and my
limited time. I may decide to take it up again in the future, though, in my spare time.





