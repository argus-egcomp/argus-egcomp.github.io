# Argus: Edge Computing for Video Analysis

* Qiaoyu Deng (qdeng@andrew.cmu.edu) 
* Changkai Zhou (zchangka@andrew.cmu.edu)


## SUMMARY

We are going to implement a possible optimized CNN computing algortihthms in parallel for a real-time computer vision application on the Tegra X1 in a camera in the lab. 

## THE CHALLENGE

* Describe why the problem is challenging. What aspects of the problem might make it difficult to parallelize? In other words, what to you hope to learn by doing the project?
* Describe the workload: what are the dependencies, what are its memory access characteristics? (is there locality? is there a high communication to computation ratio?), is there divergent execution?
* Describe constraints: What are the properties of the system that make mapping the workload to it challenging?



### Challenges

* The conflict between the very limitting computing resources of Tegra X1 and the requirement of real-time visual recognition
* The uncertainty of how much improvement of speed we can make on the CNN algorithm in parallel
* The difficulty of creating efficient pipeline that performs super-accurate statistics of people walking by

### Constraints
* The limits for the frequencies of use of Tegra X1 in the lab

### Workload

Order | Task | Estimated Time (h)
------|------|-----------
|1| Learn Computer Vision related knowledge|6
|2| Learn CNN for Visual Recognition|10
|3| Read and Get familiar Reference Source Code in Github|6
|4| Get familiar the developer tools and documentation of Tigra X1|10
|5| Prepare and Pre-precess Data|6
|6| Prototype with existing CNN algorithm|6
|7| Optimize CNN algorithm in parallel for limited computing resources; implement, debug, test, and recycle...|unknown (>50) 
|8| Documentation|6
|9| Routine work|5-10     
||**Total**|**>110=55x2**




## RESOURCES
Describe the resources (type of computers, starter code, etc.) you will use. What code base will you start from? Are you starting from scratch or using an existing piece of code? Is there a book or paper that you are using as a reference (if so, provide a citation)? Are there any other resources you need, but haven't figured out how to obtain yet? Could you benefit from access to any special machines?

### Hardware

* One Tegra X1 in the lab
* One Camera (providing the video data)

### Data
* The video data provided by the camera around NSH
* **[?] Online available open-source video datasets**

### Related Research (with source codes)
**Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields**

* Paper: [Here](https://arxiv.org/pdf/1611.08050.pdf)
* Source Code: [Here](https://github.com/ZheC/Realtime_Multi-Person_Pose_Estimation)


**Optimizing Deep CNN-Based Queries over Video Streams at Scale**

* Paper: [Here](https://arxiv.org/abs/1703.02529)
* Source Code
	* noscope: [here](https://github.com/stanford-futuredata/noscope)
	* tensorflow-noscope: [here](https://github.com/stanford-futuredata/tensorflow-noscope/tree/noscope)

### DL and CV Tutorials

* Deep Learning tutorial - [link](http://deeplearning.net/tutorial/)
* Stanford CS231n: Convolutional Neural Networks for Visual Recognition - [link](http://cs231n.stanford.edu/)

## GOALS AND DELIVERABLES

### Deliverables
#### Basic Plan 

* The optimized algorithm satisfy the industrial requirements of **a basic real-time visual application** on a Tegra X1 core, such as **the counting of people walking by.**
* Implement an optimized CNN parallel algorithm **stably** faster than the results in related research
* **Error-tolerant** application


#### Premium Plan

* The optimized algorithm satisfy the requirements of **a fancy and meanningful real-time visual application** on a Tegra X1 core, such as object recognition, 2D pose estimation, etc.
* Implement an optimized CNN parallel algorithm **significantly** faster than the results in related research
* **Accurate** application

#### Reference "Grading Scheme"

* The actual performance of a real-time visual application with optimized algorithm on the Tegra X1 core
* [?] other similar research


Describe the deliverables or goals of your project.

This is by far the most important section of the proposal:

* Separate your goals into what you PLAN TO ACHIEVE (what you believe you must get done to have a successful project and get the grade you expect) and an extra goal or two that you HOPE TO ACHIEVE if the project goes really well and you get ahead of schedule. It may not be possible to state precise performance goals at this time, but we encourage you be as precise as possible. If you do state a goal, give some justification of why you think you can achieve it. (e.g., I hope to speed up my starter code 10x, because if I did it would run in real-time.)
* If applicable, describe the demo you plan to show at the parallelism computation (will it be an interactive demo? will you show an output of the program that is really neat? will you show speedup graphs?). Specifically, what will you show us that will demonstrate you did a good job?
* If your project is an analysis project, what are you hoping to learn about the workload or system being studied? What question(s) do you plan to answer in your analysis?
* Systems project proposals should describe what the system will be capable of and what performance is hoped to be achieved.
* IN GENERAL: Imagine that I didn't give you a grading script on assignments 2, 3, or 4. Imagine you did the entire assignment, made it as fast as you could, and then turned it in. You wouldn't have any idea if you'd done a good job!!! That's the situation you are in for the final project. And that's the situation I'm in when grading your final project. As part of your project plan, and ONE OF THE FIRST THINGS YOU SHOULD DO WHEN YOU GET STARTED WORKING is implement the test harnesses and/or baseline "reference" implementations for your project. Then, for the rest of your project you always have the ability to run your optimized code and obtain a comparison.

## PLATFORM CHOICE

Depending on the hardware we choose, Tegra X1, we will use the programming languages below:

* Platform
	* Linux
* API
	* OpenGL
	* NVIDIA CUDA
* Programming Language
	* C/C++
	* Python
* Dev Tools
	* **...[need to be filled in]**


Reference: [TEGRA X1 DEVELOPER TOOLS](http://on-demand.gputechconf.com/gtc/2015/presentation/S5648-Sebastien-Domine.pdf)

Describe why the platform (computer and/or language) you have chosen is a good one for your needs. Why does it make sense to use this parallel system for the workload you have chosen?

## SCHEDULE
4.10 - 5.8, 4 weeks

Week | Order | Task | Estimated Time (h)
-----|------|------|-----------
|0-1|1| Learn Computer Vision related knowledge|6
||2| Learn CNN for Visual Recognition|10
||3| Read and Get familiar Reference Source Code in Github|6
||4| Get familiar the developer tools and documentation of Tigra X1|10
|1-1.5|5| Prepare and Pre-precess Data|6
||6| Prototype with existing CNN algorithm|6
|1.5-3.5|7| Optimize CNN algorithm in parallel for limited computing resources; implement, debug, test, and recycle...|unknown (>50) 
|3.5-4|8| Documentation|6
||9| Routine work|5-10     
||| **Total**|**>110=55x2**