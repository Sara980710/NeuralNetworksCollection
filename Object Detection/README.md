# Object detection
## One stage detectors
* CenterNet
  * Anchor-free
* CornerNet
  * Anchor-free
* FCOS
  * Anchor-free
* OverFeat
* RetinaNet (2017) - <a href="https://openaccess.thecvf.com/content_iccv_2017/html/Lin_Focal_Loss_for_ICCV_2017_paper.html" target="_blank">report</a> - <a href="https://www.youtube.com/watch?v=infFuZ0BwFQ" target="_blank">youtube</a>
  * First one stage detector that outperformes two stage detectors
  * Uses focal loss function 
  * **QUESTION: Can you use threshold instead of pushing down the graph in focal loss?**
* SSD
* YOLO (2016) - You only look once - <a href="https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Redmon_You_Only_Look_CVPR_2016_paper.html" target="_blank">report</a>
  * Struggles with small objects
  * Fast but suffers on localization and recall errors
* YOLOv2/YOLO9000 (2016) - <a href="https://openaccess.thecvf.com/content_cvpr_2017/html/Redmon_YOLO9000_Better_Faster_CVPR_2017_paper.html" target="_blank">report</a>
  * Sliding anchor boxes to predict multiple shapes
  * K-means clustering to find prior box-dimensions
  * Better backbone Darknet-19
  * Hierarchical classification
* YOLOv3 (2018) - <a href="https://arxiv.org/abs/1804.02767" target="_blank">report</a>
  * Better backbone Darknet-53
* YOLOv4 (2020) - <a href="https://arxiv.org/abs/2004.10934" target="_blank">report</a>
  * Not the original YOLO creators
  * Not focusing on BFLOP
  * Targeting conventional GPU (training on sigle core)
  * State of art BoF (bag of freebies) and several BoS (bag of specials)
* <a href="https://github.com/Sara980710/NeuralNetworksCollection/tree/main/Object%20Detection/YOLOv5" target="_blank">YOLOv5</a> (2020) - no report
* PP-YOLO (2020)


## Two stage detectors
* R-CNN
* Fast R-CNN
* Faster R-CNN
* R-FCN
* Libra R-CNN
* RepPoints
  * Anchor-free

## Other
* SpineNet
* HitDetector

# Nets (Backbone of object detection)
* ConvNet GPU
* CSP (Cross Stage Partial) - <a href="https://openaccess.thecvf.com/content_CVPRW_2020/html/w28/Wang_CSPNet_A_New_Backbone_That_Can_Enhance_Learning_Capability_of_CVPRW_2020_paper.html" target="_blank">report</a>
  * less parameters and less FLOPS
  * Based on DenseNet
* DarkNet
* DetNAS
* DenseNet GPU
* DetNet
* EfficientNet
* MobileNet CPU
* MobileNetV2
* ResNet GPU
* ResNeXt GPU
* ShuffleNet CPU
* SqueezeNet CPU
* VGG GPU

# Stage feature collecting net-strucutres (Neck of object detection)
* BiFPN
* FPN (Feature Pyramid Network) - <a href="https://openaccess.thecvf.com/content_cvpr_2017/html/Lin_Feature_Pyramid_Networks_CVPR_2017_paper.html" target="_blank">report</a> - <a href="https://www.youtube.com/watch?v=mwMopcSRx1U" target="_blank">youtube</a>
  * Saves features from different scales of the image to combine them
* PAN (Path Aggregation Network)
* NAS-FPN
* SFAM
  * SE-module
* ASFF

# Increase effect of training (Augmentation)
* Photometric distortions 
* Geometric distortions
* Random erase
* CutOut
* Hide-and-seek
* grid mask
* MixUp
* CutMix
* GAN
* Hard negative example mining 
  * Only two-stage networks
* Online hard example mining - <a href="https://arxiv.org/abs/1604.03540" target="_blank">report</a> - <a href="https://www.youtube.com/watch?v=7mcvcggUtfc" target="_blank">youtube</a>
  * Only two-stage networks
* SAT (Self-Adversarial Training)
  * Introduced in Yolov4


# Loss functions
* MSE (Mean Square Error)
* Focal loss - deals with imbalance of classes
* IoU loss
* GIoU loss
* DIoU loss
* CIoU loss

# Label refinement network
* Knowledge distillation - <a href="https://arxiv.org/abs/1703.00551" target="_blank">report</a>
  * Soft labeling

# Enhance model
* SPP
  * Integrates [SPM](https://github.com/Sara980710/NeuralNetworksCollection/tree/main/Natural%20Language%20Processing/SPM) (Spatial Pyramid Matching) into CNN
* ASPP
* RFB
* SENet (Squeeze-and-Excitation) 
  * Mobile devices and not GPU
* SAM (Spatial Attention Module)
* Skip-connections
  * Residual connections 
  * Weighted residual connections
  * Multi-input weighted residual connections
  * Cross stage partial connections (CSP)

# Post processing
* NMS
* greedy NMS
* soft NMS
* DIoU NMS

# Activation functions
* ReLU
* leaky-ReLU
* PRELU (parametric-ReLU) 
  * difficult to train
* ReLU6
  * designed for quantization network
* SELU
  * difficult to train
* Swish
* Mish

# Normalization of activations 
* Batch Normalization (BN)
* Cross-GPU Batch Normalization (CGBN or SyncBN)
* Filter Response Normalization (FRN)
* Cross-Iteration Batch Normalization (CBN)
