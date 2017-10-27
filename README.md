# webcam_point_features
Detection of ORB features from online webcam imges.

https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_orb/py_orb.html

Now for descriptors, ORB use BRIEF descriptors. But we have already seen that BRIEF performs poorly with rotation. So what ORB does is to “steer” BRIEF according to the orientation of keypoints. For any feature set of n binary tests at location (x_i, y_i), define a 2 \times n matrix, S which contains the coordinates of these pixels. Then using the orientation of patch, \theta, its rotation matrix is found and rotates the S to get steered(rotated) version S_\theta.

ORB discretize the angle to increments of 2 \pi /30 (12 degrees), and construct a lookup table of precomputed BRIEF patterns. As long as the keypoint orientation \theta is consistent across views, the correct set of points S_\theta will be used to compute its descriptor.
