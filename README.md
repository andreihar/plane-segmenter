<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/andreihar/plane-segmenter">
    <img src="readme/logo.svg" alt="Logo" width="80" height="80">
  </a>
  
# Plane Segmenter



<!-- PROJECT SHIELDS -->
[![Contributors][contributors-badge]][contributors]
[![Licence][licence-badge]][licence]
[![LinkedIn][linkedin-badge]][linkedin]

**Detection and Segmentation of Planes**

Models for detecting and segmenting planes in aerial images, using techniques like Faster R-CNN and Mask R-CNN for enhanced performance and accuracy.



</div>



---



<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#run">Run</a></li>
    <li>
      <a href="#functional-areas">Functional Areas</a>
      <ul>
        <li><a href="#object-detection">Object Detection</a></li>
        <li><a href="#semantic-segmentation">Semantic Segmentation</a></li>
        <li><a href="#instance-segmentation">Instance Segmentation</a></li>
        <li><a href="#mask-r-cnn">Mask R-CNN</a></li>
      </ul>
    </li>
    <li><a href="#data">Data</a></li>
    <li><a href="#contributors">Contributors</a></li>
    <li><a href="#licence">Licence</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Plane Segmenter is the assignment project created for the course in Computer Vision in the Spring semester of 2023. The project focuses on applying deep learning techniques to solve key tasks in computer vision: object detection, semantic segmentation, and instance segmentation.

The objective of this assignment was to design and train advanced deep convolutional neural networks with PyTorch and Detectron2 to accurately detect and segment planes in high-resolution aerial images. The model started with a baseline configuration and iteratively improved through hyperparameter tuning and architectural adjustments.

By addressing these challenges, Plane Segmenter demonstrates practical applications of state-of-the-art computer vision techniques and provides insights into the effectiveness of different deep learning methods and configurations.

### Built With

* [![Detectron2][detectron-badge]][detectron]



<!-- RUN -->
## Run

Open the notebook using your choice software in a terminal or command window by navigating to the top-level project directory, `plane-segmenter`. For example, if the software is Jupyter Notebook:

```bash
jupyter notebook segmenter.ipynb
```



<!-- FUNCTIONAL AREAS -->
## Functional Areas

### Object Detection

An object detection model is built to identify planes in high-resolution aerial images using the modified iSAID dataset. The Detectron2 framework is employed to implement and train a Faster R-CNN model with a ResNet-101 backbone. Key hyperparameters are adjusted to enhance performance, and the model's effectiveness is assessed using the Average Precision (AP) metric. This approach sets the stage for improving detection capabilities in the following stages of the project.

<p align="center">
<img src="readme/object_detection.jpg" alt="Object Detection" width="450">
</p>

### Semantic Segmentation

A deep neural network is developed for semantic segmentation to identify planes in images. Segmentation masks are extracted and processed, with images and masks resized to a consistent size. The model uses an encoder-decoder architecture, where the encoder captures image features and the decoder generates the segmentation masks. Enhancements include adding layers to both the encoder and decoder, and incorporating skip connections to retain spatial information. The training employs Binary Cross-Entropy with logits as the loss function and Stochastic Gradient Descent (SGD) for optimisation. Performance is evaluated using the Intersection-over-Union (IoU) metric.

<p align="center">
<img src="readme/semantic_segmentation_1.jpg" alt="Semantic Segmentation Image" width="200">
<img src="readme/semantic_segmentation_2.jpg" alt="Semantic Segmentation Mask" width="200">
</p>

### Instance Segmentation

Instance segmentation is implemented by integrating a trained object detection model with a segmentation module to generate detailed masks for each detected instance. The approach involves using the model's predictions in place of ground-truth bounding boxes from the previous stage and processing each instance to create accurate segmentation masks. The model relies on an encoder-decoder architecture for effective feature extraction and mask reconstruction. Performance is evaluated using the Intersection-over-Union (IoU) metric, focusing on optimising model performance through careful architectural design and hyperparameter tuning.

<p align="center">
<img src="readme/instance_segmentation_1.jpg" alt="Instance Segmentation Image" width="350">
<img src="readme/instance_segmentation_2.jpg" alt="Instance Segmentation Mask" width="350">
</p>

### Mask R-CNN

In this part, we employ Mask R-CNN mode using a ResNet-50 backbone with a Feature Pyramid Network (FPN) to perform instance segmentation and compare its results with those obtained in the Instance Segmentation part. The model is fine-tuned with similar techniques to optimise performance. We visualise and evaluate the results, focusing on the advantages and drawbacks of the Mask R-CNN approach compared to the method used previously. Additionally, we compare the detection results with those from the Object Detection part to assess improvements and differences, providing insights into which method performs better and why.

<p align="center">
<img src="readme/mask_r-cnn.jpg" alt="Mask R-CNN" width="450">
</p>



<!-- DATA -->
## Data

This dataset is a modified version of the [iSAID: A Large-scale Dataset for Instance Segmentation in Aerial Images](isaid), consisting of 198 training images and 72 test images, all from the Plane category.



<!-- CONTRIBUTION -->
## Contributors

- Andrei Harbachov ([Github][andrei-github] · [LinkedIn][andrei-linkedin])



<!-- LICENCE -->
## Licence

Because Plane Segmenter is MIT-licensed, any developer can essentially do whatever they want with it as long as they include the original copyright and licence notice in any copies of the source code.



<!-- MARKDOWN LINKS -->
<!-- Badges and their links -->
[contributors-badge]: https://img.shields.io/badge/Contributors-1-44cc11?style=for-the-badge
[contributors]: #contributors
[licence-badge]: https://img.shields.io/github/license/andreihar/plane-segmenter.svg?color=000000&style=for-the-badge
[licence]: LICENSE
[linkedin-badge]: https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin]: https://www.linkedin.com/in/andreihar/
[detectron-badge]: https://img.shields.io/badge/Detectron2-5173F1?style=for-the-badge&logo=probot&logoColor=ffffff
[detectron]: https://ai.meta.com/tools/detectron2/

<!-- Technical links -->
[isaid]: https://captain-whu.github.io/iSAID/

<!-- Socials -->
[andrei-linkedin]: https://www.linkedin.com/in/andreihar/
[andrei-github]: https://github.com/andreihar