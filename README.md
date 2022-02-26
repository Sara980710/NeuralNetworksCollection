# NeuralNetworksCollection

## Object detection
### One stage detectors
* OverFeat
* RetinaNet (2017) - <a href="https://openaccess.thecvf.com/content_iccv_2017/html/Lin_Focal_Loss_for_ICCV_2017_paper.html" target="_blank">report</a> - <a href="https://www.youtube.com/watch?v=infFuZ0BwFQ" target="_blank">youtube</a>
  * First one stage detector that outperformes two stage detectors
  * Uses focal loss function 
  * **QUESTION: Can you use threshold instead of pushing down the graph in focal loss?**
* SSD
* YOLO - You only look once - <a href="https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Redmon_You_Only_Look_CVPR_2016_paper.html" target="_blank">report</a>
  * Struggles with small objects
  * Fast but suffers on localization and recall errors
* YOLOv2/YOLO9000 - <a href="https://openaccess.thecvf.com/content_cvpr_2017/html/Redmon_YOLO9000_Better_Faster_CVPR_2017_paper.html" target="_blank">report</a>
  * Sliding anchor boxes to predict multiple shapes
  * K-means clustering to find prior box-dimensions
  * Better backbone Darknet-19
  * Hierarchical classification
* YOLOv3 - <a href="https://arxiv.org/abs/1804.02767" target="_blank">report</a>
  * Better backbone Darknet-53


### Two stage detectors
* R-CNN
* Fast R-CNN
* Faster R-CNN

## Other 2D Network-structures
* FPN (Feature Pyramid Network) - <a href="https://openaccess.thecvf.com/content_cvpr_2017/html/Lin_Feature_Pyramid_Networks_CVPR_2017_paper.html" target="_blank">report</a> - <a href="https://www.youtube.com/watch?v=mwMopcSRx1U" target="_blank">youtube</a>
  * Saves features from different scales of the image to combine them
