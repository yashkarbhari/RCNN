# RCNN Implementation
Computer vision as we know always move around classification and object detection and hence discussing some of the early breakthroughs are pretty sure helpful in understanding modern research. R-CNN was one of the first approach to discuss detection through convolution. Instead of using huge number of proposals R-CNN uses only first 2000 of them, which make it faster than other approches available at that time.

This is a aircraft detection from satellite images dataset with the goal of detecting the aircraft with a bounding box using the RCNN model.
 
 ![](Images/1.png)
 ![](Images/2.png)
 
 ![](Images/3.png)
 ![](Images/4.png)
 
 1) First step- Running selective search on indvidual image to obatain region proposals(2000 here).
 2) Second step- Classifying region proposals as positive and negative example based on IOU(IOU explained properly in notebook itself).
 3) Third step- Passing every proposal through pretrained network on some image dataset(We use VGG 16 trained on ImageNet) to output a fixed size feature vector(4096 here).
 4) Fourth step- Using Bounding Box Regression for better results.
 
 __NOTE__: We can increase the accuracy of the model by increasing the epochs or, doing data augmentation or, tuning the hyperparameters, I have not done hyperparameter tuning because the main goal of doing this was not to show accuracy but to understand RCNN and implementing it, you can tune it to get better results.
 
 ### How RCNN works?
 
