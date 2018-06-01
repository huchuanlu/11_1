This is a MATLAB implementation of the superpixel based tracking method proposed by

Shu Wang, Huchuan Lu, Fan Yang, Ming-Hsuan Yang, "Superpixel Tracking", 13th International Conference on Computer Vision (ICCV2011), pp. 1323-1330, 2011. 

The code has been tested with MATLAB R2012a and 64-bit Windows 7/8. Since the executable binary for generating superpixels is built on a Windows machine, our implementation cannot run with Linux systems. It may also encounter some compatible issues with old versions of MATLAB.
  
==============================================
HOW TO RUN THE CODE
==============================================

We include a testing sequence "bird2" in the data folder so you can simply run runTracker to see how the tracker works. If you want to run our code on your own sequence, please follow these steps:

1. open trackparam, add the name of the sequence to the list of sequences and add necessary parameters such as coordinates of the initial bounding box and particle sampling parameters. You can refer to the comments for help.

2. change dataPath to the path of your sequence which contains images of all frames. The naming of the images should follow the format 000n.png/jpg/bmp which has 4 digits with 0 padding at the beginning.

3. type runTracker to run the tracker.

4. all results are saved in the "results" folder under the same path of the sequence.

==============================================
UPDATE LOG
==============================================

V2.3 3013.12.3
Modified to handle grayscale images.

V2.2 2013.9.14
Parameters are fixed for testing sequences.
Adopted the pairwise distance computation code by Dahua Lin (http://www.mathworks.com/matlabcentral/fileexchange/15935-computing-pairwise-distances-and-metrics) to compute the distance between color histograms.
Improved the efficiency of color histogram computation and interpolation.

V2.1 2012.9.7
A small bug related to handling the number of superpixels is fixed. Thanks to John Lin for helping us find this bug.

V2.0 2012.6.22
More comments are added.
Code is reorganized to improve the readability.

V1.0 2012.5.3
Preliminary version released.

==============================================
NOTICE
==============================================

This implementation is still a preliminary version. We are working on it to improve the efficiency and readability.

Due to the limitation of the SLIC segmentation code, you may need to choose a small number of superpixels to prevent an error from the SLIC code when the size of the bounding box is very small. We will address this issue in the future version.

Any questions please contact us by
deartonyw@gmail.com or fyang@umiacs.umd.edu