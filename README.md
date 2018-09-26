# High-resolution fingerprint recognition
This repository contains the original implementation of the fingerprint pore detection and description models from [CNN-based Pore Detection and Description for High-Resolution Fingerprint Recognition]() (Submitted to WACV 2019).

## PolyU-HRF dataset
The Hong Kong Polytechnic University (PolyU) High-Resolution-Fingerprint (HRF) Database is a high-resolution fingerprint dataset for fingerprint recognition. We ran all of our experiments in the PolyU-HRF dataset, so it is required to reproduce them. PolyU-HRF can be obtained by following the instructions from its authors [here](http://www4.comp.polyu.edu.hk/~biometrics/HRF/HRF_old.htm).

Assuming PolyU-HRF is inside a local directory named `polyu_hrf`, its internal organization must be as following in order to reproduce our experiments with the code in this repository as it is:
```
polyu_hrf/
  DBI/
    Training/
    Test/
  DBII/
  GroundTruth/
    PoreGroundTruth/
      PoreGroundTruthMarked/
      PoreGroundTruthSampleimage/
```

## Requirements
The code in this repository was tested for Ubuntu 16.04 and Python 3.5.2, but we believe any newer version of both will do.

We recomend installing Python's virtualenv (tested for version 15.0.1) to run the experiments. To do it in Ubuntu 16.04:
```
sudo apt install python3-virtualenv
```

Then, create and activate a virtualenv:
```
python3 -m venv env
source env/bin/activate
```

To install the requirements either run, for CPU usage:
```
pip install -r cpu-requirements.txt
```
or run, for GPU usage, which requires the [Tensorflow GPU dependencies](https://www.tensorflow.org/install/gpu):
```
pip install -r gpu-requirements.txt
```