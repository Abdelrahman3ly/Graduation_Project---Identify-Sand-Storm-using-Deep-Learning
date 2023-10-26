# Graduation_Project---Identify-Sand-Storm-using-Deep-Learning

### Project Defination
------------------------
Sandstorms, also known as dust storms, occur when strong winds pick up and carry large amounts of sand and
dust particles, often resulting in reduced visibility and air quality. Sandstorms can severely impact agriculture, infrastructure, and human health, making early detection crucial.

Original Image

![10](https://github.com/Abdelrahman3ly/Graduation_Project---Identify-Sand-Storm-using-Deep-Learning/assets/67483743/0ccfaa73-9159-4c04-8b91-43061b294461)

Mask Image

![10_GT](https://github.com/Abdelrahman3ly/Graduation_Project---Identify-Sand-Storm-using-Deep-Learning/assets/67483743/b10fe5c2-3e88-4659-9f3c-0cf8956eedd2)


### Used Models
---------------
Semantic image segmentation models, specifically U-Net and DeepLabV3, for detecting and monitoring sandstorms.  Traditional methods using ground-based sensors and meteorological data have limitations, leading to the use of satellite or aerial images for better spatial coverage and accuracy.

#### U-Net
-----------
U-Net, a model used for image segmentation, in detecting and segmenting sandstorms. While U-Net has been widely used in fields like medical imaging, remote sensing, and computer vision, its use in sandstorm detection is limited.

Key findings from various studies include :-
----------------------------------------------
  - A deep learning-based approach using U-Net achieved 87% accuracy in detecting sandstorms from satellite images.
  - Another study applied transfer learning to a pre-trained U-Net model for sandstorm segmentation in satellite images, yielding promising results.
  - A modified version of U-Net, which incorporated temporal information, was used for sandstorm detection in videos from a ground-based camera, improving the     
    model’s performance.
    
    ![u-net-architecture](https://github.com/Abdelrahman3ly/Graduation_Project---Identify-Sand-Storm-using-Deep-Learning/assets/67483743/c3780d75-ccff-4b6f-b130-1146ab7d1ded)


#### DeepLabV3+
----------------
DeepLabV3, the predecessor of DeepLabV3+, is designed to handle the problem of segmenting objects at multiple scales. It employs atrous convolution in cascade or in parallel to capture multi-scale context by adopting multiple atrous rates3. The Atrous Spatial Pyramid Pooling (ASPP) module from DeepLabV2 is augmented with image-level features encoding global context to further boost performance3.

DeepLabV3, a semantic segmentation model, in various fields :-
----------------------------------------------------------------
##### High-resolution Satellite Images:
A study proposed a modified version of DeepLabV3 for semantic segmentation of high-resolution satellite images. The researchers introduced a novel multi-scale fusion module to enhance the model’s accuracy and efficiency.
##### Autonomous Driving:
DeepLabV3 was used for semantic segmentation of urban scenes in autonomous driving scenarios. The model was refined using atrous spatial pyramid pooling and conditional random fields.
##### Remote Sensing Images: 
In another study, DeepLabV3 was used for vegetation segmentation in remote sensing images. The researchers fine-tuned the pre-trained DeepLabV3 model using transfer learning, achieving state-of-the-art results.

![My project-1](https://github.com/Abdelrahman3ly/Graduation_Project---Identify-Sand-Storm-using-Deep-Learning/assets/67483743/c64fef27-4ec6-4a14-8603-c92ccb34a1fd)


### Result
------------
##### Comparison between real dataset and augmented dataset
---------------------------------------------------------------
We conducted experiments using two datasets, one real and one artificially augmented and compared the performance of two state-of-the-art models, U-Net and DeepLabV3.



                            |     Dataset        |    Performance    |        U-Net      |       DeepLapV3      |
                            |--------------------|-------------------|-------------------:----------------------|
                            |      Real          |     Accuracy      |        77%        |         81%          |
                            |                    |       MIOU        |        72%        |         76%          |
                            ------------------------------------------------------------------------------------|
                            |      Augmented     |     Accuracy      |        91%        |          94%         |
                            |                    |       MIOU        |        85%        |          89%         |


                                                    Table 1: Impact of data augmentation

            
Table 1 shows that both U-Net and DeepLabV3 achieved high accuracy on the real dataset, with DeepLabV3
performing slightly better than U-Net. On the augmented dataset, both models achieved even higher accuracy, with
DeepLabV3 outperforming U-Net. This suggests that data augmentation can significantly improve the performance
of image segmentation models.


##### Comparison between dependent dataset and independent dataset
--------------------------------------------------------------------
We compared the performance of the models on the dependent dataset and the independent dataset. The dependent dataset was generated by randomly splitting the original dataset into training and validation sets, while the
independent dataset was obtained from a different source.


                            |     Dataset        |    Performance    |        U-Net      |       DeepLapV3      |
                            |--------------------|-------------------|-------------------:----------------------|
                            |     Dependent      |     Accuracy      |        91%        |         94%          |
                            |                    |       MIOU        |        85%        |         89%          |
                            ------------------------------------------------------------------------------------|
                            |     Independent    |     Accuracy      |        91%        |          93%         |
                            |                    |       MIOU        |        84%        |          88%         |

                                                      Table 2: Impact of data dependency


Table 2 shows that both U-Net and DeepLabV3 achieved high accuracy on both the dependent and independent
datasets, with DeepLabV3 performing slightly better than U-Net on both datasets. In terms of MIOU, both
models achieved high scores on the dependent dataset, with DeepLabV3 outperforming U-Net. However, on the
independent dataset, the performance of both models dropped slightly, with U-Net performing slightly worse than
DeepLabV3.

### Conclution
----------------
In this project , we will compare U-Net and DeepLabV3’s performance in detecting sandstorms, with DeepLabV3 outperforming U-Net due to its advanced architecture and optimization techniques. However, U-Net can be a viable option depending on the use case and resources available. The research contributes to developing accurate methods for sandstorm detection and management, ultimately aiming to reduce their environmental and health impacts.

