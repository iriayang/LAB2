## Installation


### Option 1: Step-by-step installation

```bash

conda create --name MEGA -y python=3.7
source activate MEGA

# this installs the right pip and dependencies for the fresh python
conda install ipython pip

# mega and coco api dependencies
pip install ninja yacs cython matplotlib tqdm opencv-python scipy

# follow PyTorch installation in https://pytorch.org/get-started/locally/
conda install pytorch=1.3.0 torchvision=0.4.0 cudatoolkit=10.0 -c pytorch

export INSTALL_DIR=$PWD

# install pycocotools
cd $INSTALL_DIR
git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
python setup.py build_ext install

# install cityscapesScripts
cd $INSTALL_DIR
git clone https://github.com/mcordts/cityscapesScripts.git
cd cityscapesScripts/
python setup.py build_ext install


cd $INSTALL_DIR
git clone https://github.com/iriayang/LAB2.git
cd LAB2


# re-build it
python setup.py build develop

pip install 'pillow<7.0.0'

unset INSTALL_DIR

#Download
Model | Backbone | AP50 | AP (fast) | AP (med) | AP (slow) | Link
:---: | :---: | :---: | :---: | :---: | :---: |:---:
single frame baseline | ResNet-101 | 76.7 | 52.3 | 74.1 | 84.9 | [Google](https://drive.google.com/file/d/1W17f9GC60rHU47lUeOEfU--Ra-LTw3Tq/view?usp=sharing)
**MEGA** | ResNet-101 | 82.9 | 62.7| 81.6 | 89.4 | [Google](https://drive.google.com/file/d/1ZnAdFafF1vW9Lnpw-RPF1AD_csw61lBY/view?usp=sharing)

