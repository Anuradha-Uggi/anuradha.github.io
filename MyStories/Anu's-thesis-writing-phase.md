# Chapter 1: The story of MS-NetVLAD
1. The story has began with LPIPS,NetVLAD, and Patch-NetVLAD applied to a costum dataset. Patch-NetVLAD significantly outperforms the other models but at the cost of substantially increased space and time complexity
2. Performance is great
3. We need high performance but low complexity models in practice to support real-time deployment
4. LPIPS uses features from multiple intermediate layers to boost the performance of predicted quality
5. Similarly, SIFT like classical approaches scans across multiple scales for robust features
6. In contrast, the existing VPR models rely on bottleneck features alone
7. Hypothesis is to leverage the additional information naturally captured at multiple scales of features across intermediate layers of a model
8. However, raw features can't be directly used due to following limitations: 1. high-dimensionality demanding more space and time and 2. might contain reduandant features that hurt the performance
9. To achieve these goals, we append dimensionality reduction techniques to the intermediate slices (a block of layers) of the backbone model, and finetune the model on the VPR specific datasets to adapt the model to the VPR task
10. This we call MS-NetVLAD, which significantly imroves over the NetVLAD model and peforms competitively with the SOTA models like Patch-NetVLAD, MixVPR, and R2former
11. Experiments — Results — Discussion

