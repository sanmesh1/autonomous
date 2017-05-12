# FUBAR Labs Autonomous PowerWheels Racing

Simple model in `basic_model.py`.  Currently linear with mean squared error loss (summed over outputs?)

## Inputs

* Webcam image
* Current Accel
* Current Speed

## Future Inputs
* Current Distance from rangefinder
* Current Steering wheel angle

## Outputs

* Steering Wheel angle
* Maybe speed?

# Data sources

* [DeepDrive](http://deepdrive.io)
  * [Compressed subset of DeepDrive](https://drive.google.com/open?id=0B0zbVEese408WjYtWGdJWTF0Rjg)

# Notes

Driving model is in `comma/otto_model.py`, I think.  Weights are...somewhere, on the old Tegra board?  Maybe use one of the weights in the DeepDrive set on the google drive.

```python
#Python Libraries
import os
import math
import numpy as np
import h5py
import glob
import scipy
import scipy.misc
import random

import argparse
```

