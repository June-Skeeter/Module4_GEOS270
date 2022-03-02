---
layout: default
title: Acquire Data
parent: Lab Application
nav_order: 2
---

# Acquire Data
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Download the Project

[Download the Project!](https://github.com/June-Skeeter/Module4_GEOS270/blob/main/data/PA_Risk_Assessment.zip){: .btn .btn-blue }

I've gotten the ball rolling for you and setup a project.  This project folder contains:

* **PA_Risk_Assessment.gdb**

  * **PA_Risk_Assessment_Inputs**: A feature dataset where you will put all the vector inputs for the project.  It already contains one layer.
    * **Waterbodies**: A polygon representing the coastline.  

  * **PA_DEM_ProjectRaster**: A Digital Elevation Model (DEM) is a type of raster data used to represent elevation.  This one covers the the Port Alberni area.  Raster data *cannot* be stored in feature datasets, they are only for vector data.


* **PA_Risk_Assessment.tbx**:  Toolboxes can contain custom models and scripts.   
  * **InundationZone**: A model that you can use identify areas at risk for Tsunami inundation.  You will use this model to identify possible areas in the city that will flood.

  * You will also create a new model to incorporate data from the City of Port Alberni, the Province of British Columbia, and Statistics Canada.  This model will overlay datasets to identify which areas are at risk of flooding.

# Port Alberni Data

Download the [PA_Data.zip](https://github.com/June-Skeeter/Module4_GEOS270/blob/main/data/PA_Data.zip) and extract it to your PA_Risk_Assessment folder.  This folder contains:
* **Properties.shp** (properties in the city by zoning type) which you should import into the PA_Risk_Assessment_Inputs feature dataset.  
* Two text files:
 * **ZoningCodes** is metadata for Properties.shp.  We don't need to worry about it for now.  
 * **Shelters.csv** is a text file with the Lat/Lon coordinates of the tsunami shelters.  **See the video below** for instructions on how to import point data from text files so you can import the Shelters layer into the PA_Risk_Assessment_Inputs feature dataset.

**Note** In the videos, the project is refereed to as Module5, but I've changed it to PA_Risk_Assessment.  Everything else is still the same.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KTZ5ix_O8Wo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>




# Downloading Census Data

We want to to download Dissemination Area level population data for the Port Alberni using [Simply Analytics](https://resources.library.ubc.ca/page.php?id=1044).  The video below can help guide you through the download process.  We are going to download two population variables:

* **Total Population**
* **Total Households**

<iframe width="560" height="315" src="https://www.youtube.com/embed/Pe6xiF22kRs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Import the Census Data


**1**{: .label .label-red } Once you have downloaded the data, extract it to your PA_Risk_Assessment folder.  

**2**{: .label .label-red } Import the Simply Analytics shapefile into the PA_Risk_Assessment_Inputs feature dataset.  Name it **Population_Data** 

**3**{: .label .label-red } Make sure to set the field names following the same procedure as in Module3, reference the **variables_names.txt**.  
* **Note**: It appears there is a bug in ArcPro, that sometimes causes issues renaming variables while importing Feature Classes.  Open the attribute table of Population_Data once you've imported it and check that the Population and Household names transferred.  If you see VALUE0 and VALUE1 instead, you can manually set names by right clicking on the column you want to rename >> click Field >> Edit the Aliases in the dialog that opens, then save the edits.  You can ask your TA for help if you get stuck here.


# Downloading Roads Data from DataBC

To conduct the analysis, we also need a roads layer.  This data set is available for download from [DataBC](https://www.data.gov.bc.ca/).  DataBC is a useful website for downloading a number of dataset from across the province.  Follow the video instructions to download the roads layers.  Make sure you download the layer **Digital Road Atlas (DRA) - Demographic Partially-Attributed Roads**

**1**{: .label .label-green } You will be emailed a link to download the data.  Extract the file to your PA_RiskAssesment project folder then import the data into your PA_RiskAssesment_Inputs feature dataset.  Name it **PA_Roads**.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hL7ga4EnMB4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


