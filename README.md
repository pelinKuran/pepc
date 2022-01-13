<div id="top"></div>


<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">PEPC</h3>

  <p align="center">
    PEPC is a libary that contains several image processing applications, and my Bachelor Final Project.   

</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a> 
      <ul>
        <li><a href="#built-with">Built With</a></li>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li>
         <a href="#project-details">Project Details Steps</a>
    <ul>
        <li><a href="#development-steps">Development Steps</a></li>
        <li><a href="#usage">Usage</a></li>
    </ul>
    </li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

PEPC has 4 different capabilities. These are
* Pattern Evaluation
* Pattern Matching
* Natural Feature Marker Pose Calculation 6 DoF
* Cross Correlation Calculation using Template Matching

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With
* [C++ (ISO C++14 Standard) ](https://isocpp.org/wiki/faq/cpp14)
* [OpenCV](https://opencv.org/)
* [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
### Prerequisites
Make sure you fulfilled the prerequisities before using the library.
* OpenCV 4.5.3
* C++ (ISO C++ 14 Standard)
* Tesseract 4.1

## Project Details

### Development Steps
In this section I listed development stages of the PEPC library. 

1. I made lots of research about template matching, pattern matching algorithms. 
2. I implemented OpenCV's pattern matching tutorials before I customized them for my purpose.
3. I developed pattern matching algorithm using OpenCV's documentations and tutorials.
4. I made researches about pose calculation and studied fundementals of image processing using the course <a href="https://www.udacity.com/course/introduction-to-computer-vision--ud810">Introduction to Computer Vision. </a>

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
### Usage

Let's talk what this library capable of!

* Pattern Evaluator:
This brings ability to check few properties of the image target, which intended to be used as a natural marker. By checking properties that are likely to effect tracking quality PEPC may give feedback about the quality of the pattern. These properties may listed as,
    Checking,
    - brightness of the environment
    - total keypoints found in the image
    - total inliers number
    - selected pattern to frame size ratio
    
 * Matching Algorithm:
 This algorithm is developed using ORB keypoint extractor, BRIEF descriptor, MAGSAC++ estimator. It tracks pattern by matching keypoints from the captured frame during run time.
 
 * Pose Calculation:
 After having PEPC's pose calculation algortihm, you will be able to use naturaş feature markers to calculate camera pose in 6 dof.
 
 * Finding Dissimilarity:
 It is possible to determine two different states of a product (such as switch open or switch close) by using OpenCV's template matching alogrithm. It does provide cross correlation of given two images. Here I used tesseract library to read numbers on switch and tried to use them as their ID. 
 
 - I build tesseract using vcpkg. `vcpkg install tesseract:x64-windows-static`

## Acknowledgements
I would like to thank to my supervisor Resul Aydoğan and Sefa Ödemiş for all their help and advice with this work. I would also like to thank rest of the HARF team for their support during my co-op journey.
