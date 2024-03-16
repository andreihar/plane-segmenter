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

**Taiwanese Hokkien transliterator from Chinese characters**

It has methods that allow to customise transliteration and retrieve any necessary information about Taiwanese Hokkien pronunciation.<br />
Includes word tokeniser for Taiwanese Hokkien.

[Report Bug][bug] •


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
    <li>
      <a href="#features">Features</a>
      <ul>
        <li>
          <a href="#questions-creation">Questions Creation</a>
          <ul>
            <li><a href="#audio-recorder">Audio Recorder</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#install">Run</a></li>
    <li>
      <a href="#usage">Usage</a>
      <ul>
        <li>
          <a href="#converter">Converter</a>
          <ul>
            <li><a href="#system">System</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#example">Example</a></li>
    <li><a href="#data">Data</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
    <li><a href="#licence">Licence</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Memory Lane is the final project created by members of the ItJustWorks team for the course in Introduction to Software Engineering in the Summer semester of 2022. The theme of the course was agile software development in three sprints of the Android mobile application that should enhance the lives of people diagnosed with dementia, particularly the elderly.

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
<img src="readme/overview.jpg" alt="Overview" height="450">
</p>

### Semantic Segmentation

A deep neural network is developed for semantic segmentation to identify planes in images. Segmentation masks are extracted and processed, with images and masks resized to a consistent size. The model uses an encoder-decoder architecture, where the encoder captures image features and the decoder generates the segmentation masks. Enhancements include adding layers to both the encoder and decoder, and incorporating skip connections to retain spatial information. The training employs Binary Cross-Entropy with logits as the loss function and Stochastic Gradient Descent (SGD) for optimization. Performance is evaluated using the Intersection-over-Union (IoU) metric.

<p align="center">
<img src="readme/matches.jpg" alt="Matches" height="450">
</p>



<!-- DATA -->
## Data

This dataset is a modified version of the [iSAID: A Large-scale Dataset for Instance Segmentation in Aerial Images](isaid), consisting of 198 training images and 72 test images, all from the Plane category.



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
[bug]: https://github.com/andreihar/plane-segmenter/issues
[isaid]: https://captain-whu.github.io/iSAID/

<!-- Socials -->
[andrei-linkedin]: https://www.linkedin.com/in/andreihar/
[andrei-github]: https://github.com/andreihar