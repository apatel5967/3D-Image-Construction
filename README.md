# 3D-Image-Construction
This code is meant to recreate a 2D image into a 3D representation. Two images are given of the same object, but from different angles. By analyzing the relative positions of corresponding points in the two images, the 3D coordinates of the scene points can be reconstructed using triangulation.

Keypoints are found in both images and lines are drawn between them. Then, RANSAC is implemented to match the best points between the images and remove an outliers. 

The essential matrix matrix E is then computed from the inlier matches, and it is used to find the relative rotation and translation between the two camera views. After that, the matrix is decomposed to find the four possible combinations of rotation and translation of the poses of the two cameras. 

Following this, linear triangulation is used to reconstruct 3D points from the matched keypoints using the camera poses from earlier. Lastly, the 3D points are then visualized.
