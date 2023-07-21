---
title: Technical considerations for selection of a tablet for Avare
date: 2023-07-21
layout: post
tag: Tablet
tag: Technical
author: Peter A. Gustafson
---

# Source

This post reformats the [original post to the user mailing
list](https://groups.google.com/g/apps4av-forum/c/2HmsNbsiqrQ/m/69MwWP3ACwAJ)
which is now old (2016). Nevertheless, the technical arguments are
still true.

# Original post

## Intro

**pballer2oo7 and all.**

Herein contains my wearisome dissertation on _"plate quality"_, which
really should be referred to as _image rendering_.

pballer, the screenshot image isn't clear. I agree the 5 could be
mistaken for a 6.

![Submitted Screenshot](images/Screenshot_20160902-164508-pballer2oo7.webp)

**HOWEVER: Screenshots mislead.**

This isn't simply a "better for me is better for all" type of request.
Attached is the real plate image (rather than the screenshot). It is
legible to me on any appropriate screen. (Not saying it couldn't be
better... but it is legible.)

![OWP VOR-DME-A 2016](images/Plate-OWP-VOR-DME-A-2016.png)
![OWP RNAV-GPS-RWY 2023](images/Plate-OWP-RNAV-GPS-RWY-17-2023.png)

pballer, you are zoomed out on a low resolution screen (which I gather
is 1024x768). The display area of the chart is probably something more
like 900x700. The native image is 1275x844. Which means each of your
screen pixels is about 1.25 real pixels. The view on screen is actually
an interpolation among the pixels that surround it in the image file.
(To imagine this, pretend I'm your tablet. I'll take 0.27778 of each
pixel above and below on the left, and 0.22222 of the pixels above and
below on the right side. Add these together, and render. Note I'll do
unique ratio left/right and up/down for each pixel. This description is
oversimplified but not inaccurate.)


## How can this be fixed???

There are two things we can do with Avare to make it look better:

-   Native vector formats such as pdf will look as good as possible...
	they draw pixels based on the vector and will be "sharp" for the
	screen quality. For the moment lets assume that is out. Avare will
	not be implementing pdf files (for now, for performance and other
	reasons previously discussed.
-   Increase image resolution. I would be OK with this generally (I
	have purchased recent and very capable hardware, older harder
	would be harmed). BUT, this will barely help you pballer! To make
	it look good on your screen (as you've got it configured for zoom
	out), we would have to almost double the linear resolution. Say,
	increase it so there was a direct 2:1 ratio of image:render pixel
	ratio. This would look better...  essentially averaging 4 image
	pixels to render one screen pixel... but with as few screen pixels
	as you have, it will still not look "great".  And many users would
	not like this as it consumes 4x the resources.  Probably pballer's
	hardware would suffer more than most, (I'm extrapolating from
	knowledge of your screen resolution to the components of modern or
	older tablets with this resolution).

Beyond that, we at Apps4Av can't do much. The algorithms for pixel
rendering are well developed and implemented at the OS level.

## Options for poor quality screens

pballer, There are several things things you can do:

-   Zoom more advantageously... for example zoom OUT to a 1:1
	image:render ratio (or another whole integer ratio). The image
	will be more sharp, but would of course be smaller and perhaps
	less legible. OR zoom IN to a 1:2 ratio. You would loose much of
	your image off the edge, which you will not like. Either way you
	will not be satisfied.
-   Buy a better tablet. Good hardware is good hardware. Cheap
	hardware is cheap. 1024x768 was good 5-8 years ago...[^1]. and is
	in many very cheep devices now. Go buy a high resolution tablet
	and things will look significantly better. As your hardware
	appears to be cheap, you live with the associated compromises.
-   Use vector based approach plates in a vector based app... for the
	moment that means something other than Avare. And by the way... it
	still won't be "perfect" on your screen because of aspect ratio!
	More on that in a minute.

[^1]: This referenced tablets made around 2010.

Note this logic applies for en-route charts too... we ship them at the
_highest_ resolution supplied by the FAA. pballer, to get a wide
enough view for your intended purpose on the chart, you have to zoom
out. Your zoom most likely results in a disadvantageous image:render
pixel ratio.  (Or, in the extreme case, actually loads a reduced
resolution image meant for overviews.) You say these en-route charts
are barely usable...  I say it is your screen, not my chart. :)

## My recommendation for hardware?

I'll tell you what I did.

I "single purpose" shopped for an Avare tablet. No other app matters
to me. (OK... that last bit is overstating. Good for Avare is probably
good enough for everything else.)

I bought one with 2560x1600 screen (A galaxy tab S 8.4). Why? I
downloaded Avare on each modest performance (or better) android tablet
at the store. The tab 8.4 was specifically formatted well for
displaying approach plates (high resolution screen, good aspect ratio
for plates). 2560/1600=1.6. Plates from the FAA come at 1.5360. The
1.6 aspect ratio shows essentially the whole plate, even after leaving
a little room for the Avare tabs etc at the top and bottom of the
screen.  Very little wasted real estate, sharp enough image.

Note: we ship Avare plate images with a vertical resolution of 1238.
So, 1238*2=2476 pixels. less than my screen resolution... So I get an
integer 1:2 image:render (linear) ratio... (that means 4 screen pixels
per image pixel).

I passed on some other very "nice" tablets, which others would have
drooled over for some "superior" spec. Those tablets I dismissed had a
different screen format... lower resolution maybe, but more critically
a different aspect ratio. For example pballer's is 1275x844=1.3333.
Zooming to something "comfortable" looses key info at the top and
bottom of the plate (or zooms out to be waste lots of screen space).
[pballer's problem is two fold... bad aspect ratio and low
resolution].  So, bottom line, there were some great high res tablets
I rejected because they zoom disadvantageously when looking at Avare
plates.  Definitely don't buy a 1.333 aspect ratio at low res if you
want to use approach plates.

If the tablet shows Avare's plates well... it will have good looking
charts too.

So I recommend single-purpose shopping based on plate rendering.

**Pete**
