---
layout: single
title: "Multi-Temporal UAV Change Detection and Dense Displacement Mapping for Monitoring a Complex Landslide"
permalink: /project2/
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/header_project2.jpg
  caption: "Photo caption here"
---
.

## Project Overview

What to write:

- general context: why landslides are hazardous and why monitoring is needed
- why remote sensing or repeated imagery is useful
- what makes this case study interesting
- the motivation for comparing different dates
- why both change detection and dense displacement are useful together

A good closing paragraph for the introduction:

- define the objective of the internship
- define the main research or technical questions

Example questions:

- Can repeated orthomosaic images detect spatial and temporal changes in the landslide?
- Can dense displacement fields help identify the direction and intensity of movement?
- How large is the uncertainty of the image-based measurements?
- How do rainfall patterns relate to observed changes?

### Study Area

What to write:

- geographic location
- geomorphological setting
- slope and terrain conditions
- why the area is unstable
- relevant events or known activity

Useful figures:

- location map
- orthomosaic overview
- map showing stable area and unstable sub-areas

## Objectives

Example:

`To develop and assess an image-based workflow for monitoring landslide change and displacement through time.`

### Specific Objectives

Examples:

- align multi-temporal images using stable terrain
- detect change areas between consecutive dates
- compute dense displacement fields
- estimate uncertainty from stable terrain
- compare activity between unstable sub-areas such as flank and flux
- relate temporal behavior to precipitation

## Data

Describe:

- image source
- spatial resolution
- dates used
- coordinate system
- stable area shapefile
- flank and flux analysis polygons
- precipitation dataset and station information

Possible table:

- date
- image file name
- temporal interval from previous image
- remarks

## Methodology

This is one of the most important sections.

A strong structure would be:

### 7.1 Workflow Overview

Start with a diagram of the pipeline:

1. image loading
2. stable-area alignment
3. common extent definition
4. radiometric correction
5. change detection
6. dense displacement estimation
7. uncertainty analysis
8. temporal analysis by area
9. precipitation comparison

### 7.2 Fine Alignment of Images

What to explain:

- why alignment is necessary
- why stable terrain is used instead of the whole image
- SIFT keypoints and matching
- homography and RANSAC
- how alignment quality is checked using residual differences or MAE

What to show:

- stable mask on reference image
- detected keypoints in stable terrain
- difference before and after alignment

### 7.3 Pre-Processing

Explain:

- intersection of valid image extents
- cropping or common mask
- histogram matching or radiometric harmonization

State why this matters:

- reduces false differences caused by illumination changes

### 7.4 Change Detection

Explain:

- grayscale conversion
- smoothing
- image differencing
- thresholding
- morphology
- area filtering

Mention:

- how stable terrain is excluded from final unstable-area interpretation
- what the output mask represents

### 7.5 Dense Displacement Field

Explain:

- optical flow concept in simple words
- why Farneback was used
- what flow components mean
- how magnitude and direction are derived

Useful note:

- say that dense flow gives continuous motion information, while change detection gives binary affected areas

### 7.6 Uncertainty Estimation

This section is very important and makes the report stronger.

Explain:

- uncertainty from stable terrain
- false detections in stable area
- residual flow in stable area
- forward-backward consistency as pointwise uncertainty
- filtering of high-uncertainty points
- coarse-grid aggregation of reliable vectors

This is a strong contribution because it shows that the method is not just descriptive but also critically evaluated.

### 7.7 Temporal and Spatial Analysis

Explain:

- pairwise summaries through time
- comparison between flank and flux
- direction through time
- direction histograms
- recurrence maps
- mean displacement maps
- temporal variability maps

### 7.8 Rainfall Analysis

Explain:

- source of rainfall data
- daily precipitation
- cumulative rainfall between image dates
- antecedent rainfall, for example 7-day accumulation
- why rainfall may help interpret landslide reactivation

## Results

This section should present the evidence clearly.

A useful structure:

### 8.1 Alignment Results

What to present:

- visual examples
- improvement in residual error
- comments on image pairs that were harder to align

### 8.2 Change Detection Results

Present:

- maps of change masks
- tables of change area per interval
- comparison between flank and flux

### 8.3 Dense Displacement Results

Present:

- magnitude maps
- direction maps
- quiver plots
- coarse low-uncertainty vector fields

### 8.4 Uncertainty Results

Present:

- stable-area RMSE
- stable-area false-change area
- pointwise flow uncertainty
- effect of filtering high-uncertainty points

### 8.5 Temporal Behavior

Present:

- time series of change area
- time series of displacement magnitude
- time series of direction
- direction histograms by area

### 8.6 Spatial Behavior

Present:

- recurrence maps
- mean displacement maps
- temporal variability maps
- comparison between flank and flux

### 8.7 Rainfall Relation

Present:

- daily rainfall panel
- pairwise precipitation totals
- antecedent rainfall
- discuss visually whether higher rainfall aligns with stronger movement or more change

Be careful:

- do not overclaim causality unless the evidence is strong

## Discussion

This is where you interpret the results, not just repeat them.

Possible topics:

- which areas were most active and why
- whether flank and flux behave differently
- whether change masks and dense flow tell consistent stories
- whether the observed motion directions are geomorphologically meaningful
- whether rainfall appears related to increased activity
- what the uncertainty analysis reveals about confidence in the results

Also discuss limitations:

- sensitivity to illumination and vegetation
- temporal gaps between image dates
- 2D image displacement versus real 3D slope movement
- dependence on image quality and alignment
- limitations of optical flow in texture-poor zones

This section is excellent for showing critical thinking, which is very valuable in an internship report.

## Conclusions

Keep this section direct.

Summarize:

- what you built
- what worked well
- the main technical findings
- the most important geomorphic or practical insight

A good conclusion usually answers the objectives explicitly.

## References

Include:

- papers on landslide monitoring
- remote sensing and image matching references
- optical flow references
- uncertainty or validation references
- rainfall and landslide triggering literature

---

**Related Links:**
- [Back to Projects]({{ '/my-projects/' | relative_url }})
- [Contact Me](mailto:lina.perez.garcia@fu-berlin.de)
