# YOLOv4 (2020)

* CSPDarknet53 backbone
* SPP, PAN neck
* mosaic data augmentation
* K-means clustering to determine anchors

<a href="https://arxiv.org/abs/2004.10934" target="_blank">report</a>
<a href="https://blog.roboflow.com/a-thorough-breakdown-of-yolov4/" target="_blank">article on Roboflow</a>


# YOLOv5 (2020)

* CSP backbone
* PA-NET neck
* scaling, color space adjustments and mosaic data augmentation (most effect) 
* auto learning bounding box anchors

##
[Introducing YOLOv5](https://blog.roboflow.com/yolov5-improvements-and-evaluation/)

##
Quotes from [blog post](https://blog.roboflow.com/yolov5-is-here/) by Joseph Nelson and Jacob Solawetz:

“Running a Tesla P100, we saw inference times up to 0.007 seconds per image, meaning 140 frames per second (FPS)! By contrast, YOLO v4 achieved 50 FPS after having been converted to the same Ultralytics PyTorch library.”

“YOLO v5 is small. Specifically, a weights file for YOLO v5 is 27 megabytes. Our weights file for YOLO v4 (with Darknet architecture) is 244 megabytes. YOLO v5 is nearly 90 percent smaller than YOLO v4.”


##
Comparison of YOLOv4 and YOLOv5: [article](https://blog.roboflow.com/yolov4-versus-yolov5/)

"YOLOv5 trains faster on the sample task, and the batch inference (which the implementation uses by default) produces realtime results. While YOLOv4 trains more slowly, its performance can be optimized to achieve higher FPS."

"If you're a developer looking to incorporate near realtime object detection into your project quickly, YOLOv5 is a great choice. If you're a computer vision engineer in pursuit of state-of-the-art and not afraid of a little more custom configuration, YOLOv4 in Darknet continues to be most accurate."
