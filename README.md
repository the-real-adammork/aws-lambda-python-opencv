# Python OpenCV module for AWS Lambda

## Description
This is a simple script that builds a deployment package including OpenCV compatible with the AWS Lambda Python runtime for Ubuntu AMI - ubuntu/images/hvm-ssd/ubuntu-xenial-16.04-amd64-server-20170221 (ami-f4cc1de2). The dynamic library is compiled with all extended instruction sets supported by Lambda CPU and binaries are stripped to save space. You simply need to add your code inside *lambda_function.py* and possibly your haar cascades files or additional Python modules.

- Build duration: ~20 min on T2.micro / ~15 min on C4.2xlarge
- Package size without haar cascades included: 26MB
- OpenCV 3.1 by default but may work with newer

**Needs to be built on an Amazon Linux instance.**

## Module building
### Option 1: with an existing instance
- Clone repo
- Launch the script `cd aws-lambda-python-opencv-master && ./build.sh`
