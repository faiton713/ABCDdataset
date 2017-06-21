# ABCD dataset

This note describes ABCD (AIST Building Change Detection) dataset.
This dataset is a new labeled dataset, specifically geared toward constructing and evaluating damage detection systems to identify whether buildings have been washed-away by tsunami.
The paper: 

## Format
Each datum in this dataset is a pair of pre- and post-tsunami aerial image patches, and encompasses a target building at the center of the patch. These pairs were cropped from aerial images taken before and after the Tohoku earthquake.

Using this dataset, we comprehensively evaluate CNNs from a practical-application viewpoint, e.g., input scenarios (pre-tsunami images are not always available), input scales (building size varies) and different configurations for CNNs. The experimental results show that our CNN-based washedaway detection system achieves 94–96% classification accuracy across all conditions, indicating the promising applicability of CNNs for washed-away building detection.

![ensemble_](https://user-images.githubusercontent.com/13417696/27383848-b32b4e8a-56c7-11e7-8ba6-4b43ebf5bc32.png)
