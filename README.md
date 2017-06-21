# ABCD dataset

This note describes ABCD (AIST Building Change Detection) dataset.
This dataset is a new labeled dataset, specially geared toward constructing and evaluating damage detection systems to identify whether buildings have been washed-away by tsunami.
The paper: 

## Format
Each datum in this dataset is a pair of pre- and post-tsunami aerial image patches, and encompasses a target building at the center of the patch. These pairs were cropped from aerial images taken before and after the Tohoku earthquake. The pixel resolution of patches is 40 cm.

The below figure shows the representative samples in the dataset, where eight pairs are shown for "washed-away" class (left column) and "surviving" class (right column).

![patches_](https://user-images.githubusercontent.com/13417696/27384118-b5539e1e-56c8-11e7-9c0c-7d06b899763f.png){:width="100px" style="display:block;margin-left:auto;margin-right:auto;"}



----
This is a ABCD dataset meant for research purposes.

There are XXX images for each of the following classes:
- washed-away
- surviving

Each image measures XXXxXXX pixels.

The images were manually extracted from large images from the USGS National Map Urban Area Imagery collection for various urban areas around the country. The pixel resolution of this public domain imagery is 1 foot.

Please cite the following paper when publishing results that use this dataset:

Yi Yang and Shawn Newsam, "Bag-Of-Visual-Words and Spatial Extensions for Land-Use Classification," ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems (ACM GIS), 2010.

Shawn D. Newsam
Assistant Professor and Founding Faculty
Electrical Engineering & Computer Science
University of California, Merced
Email: snewsam@ucmerced.edu
Web: http://faculty.ucmerced.edu/snewsam
This material is based upon work supported by the National Science Foundation under Grant No. 0917069.
