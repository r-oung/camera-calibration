# Camera Calibration

## Usage
```shell
python calibrate images/

Intrinsic Parameters:
fx: 534.0708836434115
fy: 534.1191459522821
cx: 341.5340755262212
cy: 232.94565259795462

Distortion Coefficients:
k1: -0.29297163675274435
k2: +0.10770696223452401
p1: +0.0013103837668586803
p2: -3.110188108687015e-05
k3: +0.04347981037293046

Re-projection error: 0.023686000375385673
```

## Brief Explanation of Parameters
fx, fy Focal length
cx, cy Optical center
k1, k2, k3: Radial distortion
p1, p2: Tangential distortion

## Notes: ORB Parameters
```
# ORB Extractor: Number of features per image
ORBextractor.nFeatures: 2000

# ORB Extractor: Scale factor between levels in the scale pyramid 	
ORBextractor.scaleFactor: 1.2

# ORB Extractor: Number of levels in the scale pyramid	
ORBextractor.nLevels: 8

# ORB Extractor: Fast threshold
# Image is divided in a grid. At each cell FAST are extracted imposing a minimum response.

# Firstly we impose iniThFAST. If no corners are detected we impose a lower value minThFAST

# You can lower these values if your images have low contrast			
ORBextractor.iniThFAST: 20
ORBextractor.minThFAST: 7
```
https://github.com/raulmur/ORB_SLAM2/issues/833#issue-515672777

## Issues
Q: Pip install fails with ModuleNotFoundError: No module named 'skbuild'?
A: See https://github.com/opencv/opencv-python#frequently-asked-questions

## References
- [OpenCV Camera Calibration](https://docs.opencv.org/master/dc/dbb/tutorial_py_calibration.html)