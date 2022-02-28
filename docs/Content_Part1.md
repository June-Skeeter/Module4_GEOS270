---
layout: default
title: Spatial Analysis
parent: Lecture Content
# has_children: True
nav_order: 1
---

# Spatial Analysis Methods
{: .no_toc }


Spatial analysis methods are central to the effective application of GIS.  This lecture is a bit of an "info dump".  We'll cover lots of different methods for analyzing spatial data.  We'll build on these tools in the next two modules and talk about how we can apply them in sequence.

<!-- 
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details> -->


<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/VectorAnalysis.html" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/VectorAnalysis.html" target="_blank">View Slides in New Tab</a>


<!-- 
# Vector Methods

There are a large number of spatial operations we can do using Vector data.  Some of them are very similar can be used to complete the same task with slight changes to a workflow.  The distinctions between these tools can be subtle, but they are important.  Typically in GIS there are multiple ways to get the same answers, some "routes" are just more direct. -->

## Proximity Analysis

Sometimes, we we're interested in looking at spatial relationships within or between layers.

- [Buffer](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/buffer.htm)
	- Create polygon around a point, line, or polygon feature, using a buffer distance.
	- Can be single specified value, set using a field, **or** a [Multi-Ring Buffer](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/multiple-ring-buffer.htm) which is useful for multi-criteria buffers.

- [Select by Location](https://desktop.arcgis.com/en/arcmap/latest/map/working-with-layers/using-select-by-location.htm)
	- Useful when we don't want want to alter an input layer, but we want to check for spatial relationships.  There are many relationships we can check for:
		- Containment, Intersection, Distance Based Search Criteria


## Geometric Manipulations

These methods create new layers with altered "geometries".  Geometry is a term we use to refer to points, lines, and/or polygons in a vector layer.  

### Feature Aggregation

Many times, our data is more "complex" than we need it to be.  It is often useful to aggregate features by one or more attributes.

- [Dissolve](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/dissolve.htm)
	- Merges or "dissolves" object by attribute(s).

### Feature Overlay

Often, we have multiple data layers and we want to combine them to form a new output.

- [Clip](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/clip.htm)
	- Like a "cookie cutter", cuts one layer down to size by another
- [Intersect](https://desktop.arcgis.com/en/arcmap/latest/tools/analysis-toolbox/intersect.htm)
	- Similar to clip **but** merges attributes and splits polygons by intersection.  Can be used to overlay **two or more** layers at once.
- [Identity](https://desktop.arcgis.com/en/arcmap/latest/tools/analysis-toolbox/identity.htm)
	- Similar to intersect - merges attributes and splits polygons by intersection **but**: Can only overlay **two** layers, maintains all areas of **Input** layer and **only** the overlapping portions of **Identity** feature.
- [Union](https://desktop.arcgis.com/en/arcmap/latest/tools/analysis-toolbox/union.htm)
	- Similar to identity **but** maintains all areas of **all** input layers.  Can be used to overlay **two or more** layers at once.
- [Erase](https://desktop.arcgis.com/en/arcmap/latest/tools/analysis-toolbox/erase.htm)
	- The "opposite" of clip, removes areas of one feature that overlap another.
- [Symmetric Difference](https://desktop.arcgis.com/en/arcmap/latest/tools/analysis-toolbox/symmetrical-difference.htm)
	- Similar to erase **but** keeps all non-overlapping areas of both features.
- [Spatial Join](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/spatial-join.htm)
	- Combines attributes, without altering geometry.

# Raster Methods

There are also many different types of manipulations we can do with raster data.  Because raster data is "simpler" there aren't as many tools needed to accomplish all these tasks.  Rather, we often rely on stringing together multiple computations.  Many of the complex raster analyses we can do are beyond the scope of this course, but we'll cover the basics here.

## Proximity Analysis

Sometimes, we we're interested in looking at spatial relationships using raster data.

- [Euclidean Distance](https://desktop.arcgis.com/en/arcmap/latest/tools/spatial-analyst-toolbox/euclidean-distance.htm)
	- We can use this tool to calculate distance from the nearest feature or raster layer.  

## Aggregation

Many times, our data is more "complex" than we need it to be.  It is often useful to aggregate our data.

- [Reclassify](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-analyst/reclassify.htm)
	- Reassign cell values, used to "condense" data or reassign values.

- [Mosaic](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/mosaic.htm)
	- Combine multiple raster data sets into one.  There are [multiple approaches](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/mosaic-operators.htm) we can use.


- [Zonal Statistics](https://desktop.arcgis.com/en/arcmap/latest/tools/spatial-analyst-toolbox/zonal-statistics.htm)
	- We can calculate a single statistic value (mean, max, etc.) using zones (regions) defined by and generate an output with the desired statistic by zone.  The zone can be either another raster **or** a vector layer.
	- We can also use [Zonal Statistics as Table](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-analyst/zonal-statistics-as-table.htm) to generate a table containing multiple statistics grouped by zone.

## Surface Analysis

These tools are specifically designed to analyze terrain surfaces (ie. Digital Elevation Models), however, they can be applied to other purposes in select applications.

- [Slope](https://desktop.arcgis.com/en/arcmap/latest/tools/spatial-analyst-toolbox/slope.htm)
	- Calculates the slope of a terrain surface, ie. the angle in degrees from a cell to it's "lowest" neighbor.

- [Aspect](https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/aspect-function.htm)
	- Related to slope, this tool calculates slope direction.

## Overlay

Often, we have multiple data layers and we want to combine them to form a new output.  With raster data, we have a few tools we can use for this.

- [Weighted Overlay](https://desktop.arcgis.com/en/arcmap/latest/tools/spatial-analyst-toolbox/weighted-overlay.htm)
	- Combine multiple layers for suitability or risk analysis
	- Suitable alternative for the Port Alberni Tsunami Modelling

- [Raster Calculator](https://desktop.arcgis.com/en/arcmap/latest/tools/spatial-analyst-toolbox/raster-calculator.htm)
	- More general than weighted overlay, can be used to do weighted overlay if combined with reclassification.
	- Suitable alternative for the Port Alberni Tsunami Modelling

- [Clip](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/clip.htm)
	- Cuts raster down to a bounding box.  Bounding box extent can be defined by another raster layer, a vector layer, or manually.


