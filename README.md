# ABCD dataset

This material is a description of ABCD (AIST Building Change Detection) dataset.
This dataset is a new labeled dataset, specially geared toward constructing and evaluating damage detection systems to identify whether buildings have been washed-away by tsunami.


## Description
Each datum in this dataset is a pair of pre- and post-tsunami aerial image patches, and encompasses a target building at the center of the patch.   
The below shows eight samples from the dataset, where four pairs are shown for "washed-away" buildings (left column) and "surviving" building (right column), respectively. The class label assigned to each patch (i.e. "washed-away" or "surviving") represents whether or not a building at the center of the pre-tsunami patch got wahshed-away by tsunami. 

![patches_](https://user-images.githubusercontent.com/13417696/27384118-b5539e1e-56c8-11e7-9c0c-7d06b899763f.png)

These pairs were cropped from a hefty number of RGB aerial images of Tohoku region of Japan. These aerial images were taken before or after the Great East Japan earthquake, with the original pixel resolution of 40 cm for pre-quake images and 12 cm for post-qukae images (actually, resampled to 40 cm).

As source for class labels, we employed the existing, post-quake survey result. This survey result is the outcome of an exhaustive
field investigation which was carried out under the initiative of MLIT (Ministry of Land, Infrastructure, Transport and Tourism) in the wake of the Great East Japan earthquake on March 11, 2011. As a consequence of this survey, over 220,000 buildings in the ravaged areas were assessed, and each building was assigned a label according to the degree of damage.


We prepared the patch pairs for three types of size: fixed-scale, size-adaptive and resized. Fixed-scale patches have the same resolution of the original images (40 cm) and the patch size is 160 x 160 pixels. Size-adaptive patches also have the original resolution, but were cropped depending on the size of each target building (three times larger than the target building); so the patch size varies from building to building. Lastly, resized patches are the resized version of size-adaptive patches, specifically resized to 120 x 120 pixels.  
The resulting ABCD dataset comprised 10,777 pairs for fixed-scale (4,253 washed-away) and 11,394 pairs for size-adaptive and resized (4,546 washed-away). 


Please see the following paper for further details, and cite the paper when publishing results that use this dataset:  
**Aito Fujita, Ken Sakurada, Tomoyuki Imaizumi, Riho Ito, Shuhei Hikosaka and Ryosuke Nakamura, "Damage Detection from Aerial Images
via Convolutional Neural Networks," IAPR International Conference on Machine Vision Applications (MVA), 2017.**


---

Aito Fujita  
National Institute of Advanced Industrial Science and Technology (AIST), Japan  
Email: fujita.713@aist.go.jp  

This dataset is based on results obtained from a project commissioned by the New Energy and Industrial Technology Development Organization (NEDO).
