---
title: Charts Seams in Avare
date: 2022-04-12
layout: post
tag: Sectional
tag: Chart
tag: Seams
tag: Contribute
author: Peter A. Gustafson
permalink: /chart-seams.html
---

Avare's charts are based on FAA charts. The charts distributed by the
FAA are based on a legacy system that is still being printed on paper
for sale to pilots! However, the FAA is also distributing them in a
digital form with metadata allowing them to be associated with GPS
coordinates.  **This is why creating Avare is possible!**

Contents:
* TOC
{:toc}

See our [FAA chart reference](/faa-charts-reference.html).

# The "national" sectional chart

The "national" sectional chart, updated on a [56 day
cycle](https://www.aopa.org/news-and-media/all-news/2021/february/17/vfr-charts-to-go-on-56-day-cycle-starting-february-25),
is assembled from 61
[raster](https://en.wikipedia.org/wiki/Raster_graphics) images. 

![FAA Sectional Chart Index US Contiguous](/images/FAA_SectUS_Lrg.webp)
![FAA Sectional Chart Index Alaska       ](/images/FAA_SectAK_Lrg.webp)

Though raster images are conceptually "simple" to crop, trim, and
orient, this simplicity comes at a cost. **The actual aviation data
(airport identifies, frequencies, etc) is in image form rather than
being searchable and editable data**.

The 61 individual images are regularly updated by the FAA, having
intersections and overlaps between charts.  They are stitched together
via a rough process illustrated below:

![QGIS national sectional map](/images/qgis-sectional-nationmap.webp)

# The challenge of stitching

Unfortunately, the underlying charts overlap each other, and the
aviation data placement in the region of overlap is chosen for viewing
only in one image. Hence, the actual aviation data (such as airport
identifiers and frequencies) are not consistently placed among the
images. For example, here is the intersection of:

-   Chicago
-   Detroit
-   St Louis
-   Cincinnati

![4 chart overlap](/images/section-overlaps.webp)


When the images are cropped and stitched together, the resulting image
can have **conflicts**, i.e., *some of the chart data is necessarily
lost*.

# Reconciling conflicts

**Reconciling the conflicts is a manual process.** A long term
goal of the stitching process for Avare is to **optimize the aviation
data capture**. The following illustrates the stitching around Dayton
and Columbus OH: ![Dayton and Columbus
overlap](/images/sectional-overlap-dayton-columnbus.webp)

**In this example, the stitching limits (overlayed translucent layers)
wrap around Dayton and Columbus in an effort to capture the most
essential data.** (Ideally the stitching would visually pleasing (i.e.,
not be distracting to the eye, juxtaposed elements of the overlapping
images should be harmonious rather than jarring.)

**Stitching is a moving target, as the FAA alters the
charts regularly.**

Automation of the stitching process has (so far) been
impractical. Further, it has also been impractical to monitor each
airport/frequency/landmark/etc to make sure no critical data is
trimmed. Since information that is missing is not easy to find
(especially when it is not known to be missing), this process of
finding sub-optimal stitch routing is like counting the needles in the
haystack to make sure the number is correct (and then doing it again
56 days later).

# The end result

The end result is a "national" sectional chart in Avare!  All the
Avare "national" charts (VFR, IFR, TAC, etc) are produced this way!

![Dayton Sectional](/images/Screenshot_20220412_113638_com.ds.avare.jpg)

# Found an issue?

**We rely on users to report when there are issues.**  This can be
done by making a suggestion in the
[forum](https://groups.google.com/forum/#!forum/apps4av-forum).
Ideally users would contribute fixes too! You can use
[QGIS](https://qgis.org/en/site/) and the
[Avare charts](https://github.com/gustafson/avare-charts) datasets.

<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
</style>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Needle_in_a_haystack_%282425404674%29.jpg/640px-Needle_in_a_haystack_%282425404674%29.jpg" style="width: 50%" class="center">


