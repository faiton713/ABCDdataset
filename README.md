# ABCD dataset

This material is a description of ABCD (AIST Building Change Detection) dataset.
This dataset is a new labeled dataset, specially geared toward constructing and evaluating damage detection systems to identify whether buildings have been washed-away by tsunami.

## Format
Each datum in this dataset is a pair of pre- and post-tsunami aerial image patches, and encompasses a target building at the center of the patch. These pairs were cropped from aerial images taken before and after the Tohoku earthquake. The pixel resolution of patches is 40 cm.

The below figure shows the representative samples in the dataset, where eight pairs are shown for "washed-away" class (left column) and "surviving" class (right column).

![patches_](https://user-images.githubusercontent.com/13417696/27384118-b5539e1e-56c8-11e7-9c0c-7d06b899763f.png)


Please see the following paper for further details, and cite the paper when publishing results that use this dataset:  
**Aito Fujita, Ken Sakurada, Tomoyuki Imaizumi, Riho Ito, Shuhei Hikosaka, Ryosuke Nakamura, "Damage Detection from Aerial Images
via Convolutional Neural Networks," IAPR International Conference on Machine Vision Applications (MVA), 2017.**


---

Aito Fujita  
National Institute of Advanced Industrial Science and Technology (AIST), Japan  
Email: fujita.713@aist.go.jp  

This material is based on results obtained from a project commissioned by the New Energy and Industrial Technology Development Organization (NEDO).
