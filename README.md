# ABCD dataset

This material is a description of ABCD (AIST Building Change Detection) dataset.
This dataset is a new labeled dataset, specially geared toward constructing and evaluating damage detection systems to identify whether buildings have been washed-away by tsunami.


## Synopsis of the dataset
Each datum in this dataset is a pair of pre- and post-tsunami aerial image patches, and encompasses a target building at the center of the patch.   
The below shows eight samples from the dataset, where four pairs are shown for "washed-away" buildings (left column) and "surviving" building (right column), respectively. The class label assigned to each patch pair (i.e. "washed-away" or "surviving") represents whether or not a building at the center of the pre-tsunami patch got wahshed-away by tsunami. 

![patches_](https://user-images.githubusercontent.com/13417696/27384118-b5539e1e-56c8-11e7-9c0c-7d06b899763f.png)

These pairs were cropped from a hefty number of RGB aerial images of Tohoku region of Japan. These aerial images were taken before or after the Great East Japan earthquake, with the original pixel resolution of 40 cm for pre-quake images and 12 cm for post-qukae images (actually, resampled to 40 cm).

We prepared the patch pairs for two types of size: **fixed-scale** and **resized**. Fixed-scale patches were cropped from aerial images with the fixed size of 160 x 160 pixels; so they have the same resolution of the original images (40 cm). In contrast, resized patches  were cropped depending on the size of each target building (specifically, three times larger than the target building), and then all resized to 120 x 120 pixels; so the spatial scale of the patches varies from building to building.
The resulting ABCD dataset comprised 10,777 pairs for fixed-scale (4,253 washed-away) and 11,394 pairs for resized (4,546 washed-away). 

As source for class labels, we employed the existing, post-quake survey result. This survey result is the outcome of an exhaustive
field investigation which was carried out under the initiative of MLIT (Ministry of Land, Infrastructure, Transport and Tourism) in the wake of the Great East Japan earthquake on March 11, 2011. As a consequence of this survey, over 220,000 buildings in the ravaged areas were assessed, and each building was assigned a label according to the degree of damage.


Please see the following paper for further details, and cite the paper when publishing results that use this dataset:  
**Aito Fujita, Ken Sakurada, Tomoyuki Imaizumi, Riho Ito, Shuhei Hikosaka and Ryosuke Nakamura, "Damage Detection from Aerial Images
via Convolutional Neural Networks," IAPR International Conference on Machine Vision Applications (MVA), 2017.**


## Download

ABCD dataset is available on the following link: 
> *Link to be inserted*  

The directory configuration is as follows.

```
./concat_2images/fixed_size/noMult
fixed-size (8506 = 4253 + 4253)

./concat_2images/bbox_size_resize/noMult
size-adaptive (8444: 4223 for washed-away (1) and 4221 for surviving (0))


root/fixed-scale/
     |
     |-patch-pairs/
     |     |
     |     |- image1.tif
     |     |- image2.tif
     |          :
     |     |_ image8506.tif
     |
     |_5fold-list/
           |
           |- cv1-train.csv
           |- cv1-test.csv
                :
           |_ cv5-test.csv


root/resized/
     |
     |-patch-pairs/
     |     |
     |     |- image1.tif
     |     |- image2.tif
     |          :
     |     |_ image8444.tif
     |
     |_5fold-list/
           |
           |- cv1-train.csv
           |- cv1-test.csv
                :
           |_ cv5-test.csv

```

---

Aito Fujita  
National Institute of Advanced Industrial Science and Technology (AIST), Japan  
Email: fujita.713@aist.go.jp  

This dataset is based on results obtained from a project commissioned by the New Energy and Industrial Technology Development Organization (NEDO).
