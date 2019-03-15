# ObjectDetection
An evaluation of OpenCV's object detection API for aerial tracking.

## [Object Tracking](https://github.com/Blowoffvalve/ObjectDetection/blob/master/ObjectTracking.ipynb)
In this [notebook](https://github.com/Blowoffvalve/ObjectDetection/blob/master/ObjectTracking.ipynb), i evaluate the following OpenCV Object Tracking Algorithms. 
The performance of the trackers was evaluated using 2 videos. 
For each tracker, an annotated video of the runtime statistics of the tracker's performance is linked.
  * [Boosting Tracker](https://docs.opencv.org/4.0.1/d1/d1a/classcv_1_1TrackerBoosting.html) : [Video0](https://drive.google.com/open?id=1SwmeoEPjQ5JIcKBfKp7dyigJnqwLdfqC), [Video1](https://drive.google.com/open?id=1alrXKKABXKR5_PwyLkmkDNZK65rerD8s).  
  * [MIL Tracker](https://docs.opencv.org/4.0.1/d0/d26/classcv_1_1TrackerMIL.html) : [Video0](https://drive.google.com/open?id=1ryMRNGczCenSAR5mvns3YGM48LZcsyTg), [Video1](https://drive.google.com/open?id=1djjX_H5SfUkZ2MVDGrrIweFg1IoiR_mF). 
  * [KCF Tracker](https://docs.opencv.org/4.0.1/d2/dff/classcv_1_1TrackerKCF.html) : [Video0](https://drive.google.com/open?id=12RxVT408oMzYZ31NxUvtW04FY8HhGoER), [Video1](https://drive.google.com/open?id=1DxziJwtnRt_MLhxjlwOAdN4PgsyHNtsc). 
  * [TLD Tracker](https://docs.opencv.org/4.0.1/dc/d1c/classcv_1_1TrackerTLD.html) : [Video0](https://drive.google.com/open?id=18ArDuk0KDODrBy_YJ-OyrPbLwu5YvXZx), [Video1](https://drive.google.com/open?id=1QXoTKlZbQoVQzOEUxjcCvc-S6J-o1dO9). 
  * [MEDIANFLOW Tracker](https://docs.opencv.org/4.0.1/d7/d86/classcv_1_1TrackerMedianFlow.html) : [Video0](https://drive.google.com/open?id=1VuQ7Zr0-AJ7roKU2P1hYxRnWBJ-gWv1T), [Video1](https://drive.google.com/open?id=1biNaY1P9dT6euNvI0pYvpK2UG_pdTK3F). 
  * [MOSSE Tracker](https://docs.opencv.org/4.0.1/d0/d02/classcv_1_1TrackerMOSSE.html) : [Video0](https://drive.google.com/open?id=1i41bOirKac42GGoI1vCKiFizknBZPCNT), [Video1](https://drive.google.com/open?id=168pvANqB4iZFNR9x0QtaMsORODmz0FOn). 
  * [GOTURN Tracker](https://docs.opencv.org/4.0.1/d7/d4c/classcv_1_1TrackerGOTURN.html) : [Video0](https://drive.google.com/open?id=1wTMZqz7PBsOS-OiFgHnj9zo6t-P23mQA), [Video1](https://drive.google.com/open?id=1597bDybGNsuuBu_l7z6m44fg-LY7J6O1). 
  * [CSRT Tracker](https://docs.opencv.org/4.0.1/d2/da2/classcv_1_1TrackerCSRT.html) : [Video0](https://drive.google.com/open?id=15TlNETJJBVse7HUM2FCsNPwldUZaSU3u), [Video1](https://drive.google.com/open?id=1jsX2C6lAa0LRuFr4XHfcljcabseC-iXa). 

### For the first [video](https://drive.google.com/open?id=1e9EJ7qeY1w2rHZvk3tTcQeltRNQjxt8y)

| Tracker | Average FPS | Peak FPS | Minimum FPS | Run Time(Seconds) | Average CPU % Utilization | Average Memory Utilization(GB)| Heursitic Score | Accuracy|
|---------|-------------|----------|-------------|-------------------|-------------|---------------------------|-------------------------------|---------|
|Boosting| 96.8 | 125.1 | 32.3 | 26.2 | 31.1 | 0.094 | | * |
|MIL| 19.1 | 31.3 | 12.7 | 103 | 58.4 | 0.11 | | * |
|KCF| 997 | 1098 | 497 | 8.3 | 11.5 | 0.11 | | * |
|TLD| 6.64 | 12.4 | 3.91 | 294 | 67.1 | 0.12 | | * |
|MEDIANFLOW| 465 | 1013 | 200 | 11.2 | 19.3 | 0.11 | | * |
|MOSSE|1093 | 98206.8 | 498| 7.69 | 10.2 | 0.09 | | * |
|GOTURN| 15.6** | 18.2** | 0.06** | 39.6** | 66.5** | 0.48** | ** | * |
|CSRT| 400 | 539 | 27.8 | 15.3 | 15.9 | 0.1 | | * |

>\* means the metric hasn't been implemented yet.  
>\*\* means that the tracker failed while running with an out of memory error `OpenCV(4.0.0) C:\projects\opencv-python\opencv\modules\core\src\alloc.cpp:55: 
error: (-4:Insufficient memory) Failed to allocate 39438213000 bytes in function 'cv::OutOfMemoryError'`.  

### For the second [video](https://drive.google.com/open?id=1Ra8U2T2_xEDTULJwTniY0MArzQCpzmD8)

| Tracker | Average FPS | Peak FPS | Minimum FPS | Run Time(Seconds) | Average CPU % Utilization | Average Memory Utilization(GB)| Heursitic Score | Accuracy|
|---------|-------------|----------|-------------|-------------|-------------------|---------------------------|-------------------------------|---------|
|Boosting| 48.1 | 71.5 | 25.7 | 58.3 | 31.3 | 0.13 | | * |
|MIL| 15.8 | 31.2 | 10.1 | 159 | 42.4 | 0.11 | | * |
|KCF| 411 | 569 | 38.5 | 17.2 | 18.5 | 0.11 | | * |
|TLD| 22.9 | 43.5 | 14.1 | 110 | 57.3 | 0.12 | | * |
|MEDIANFLOW| 374 | 534 | 196 | 17.6 | 19.5 | 0.11 | | * |
|MOSSE| 998 | 1131 | 333 | 12.8 | 13.9 | 0.11 | | * |
|GOTURN| 12.6** | 20 | 0.007** | 1284** | 64** | 0.5** | ** | * |
|CSRT| 28.4 | 38.5 | 17.0 | 91.6 | 48.5 | 0.12 | | * |

>\* means the metric hasn't been implemented yet.  
>\*\* means that the tracker failed while running with an out of memory error `OpenCV(4.0.0) C:\projects\opencv-python\opencv\modules\core\src\alloc.cpp:55: 
error: (-4:Insufficient memory) Failed to allocate 30453703368 bytes in function 'cv::OutOfMemoryError'`.  

Appendix:
1. Server specs
  * CPU Intel Core i7-4710MQ @ 2.50 GHz (8 CPUs).  
  * RAM 32768 MB.  
