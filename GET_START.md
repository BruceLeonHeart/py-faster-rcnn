-----------------
cuda10.2
cudnn7
cudnn8不支持
------------------
conda create -n fasterRCNN python=2.7
conda activate fasterRCNN

pip install numpy
pip install cython
pip install scikit-image
pip install protobuf==2.6.1
pip install easydict
pip install pyyaml
pip install scikit-build
pip install opencv-python==4.2.0.32
-----------------------
make all -j8
make pycaffe

----------------------------
修改文件
- lib/datasets/pascal_voc.py【类别名称】
- models/pascal_voc/VGG16/faster_rcnn_end2end/test.prototxt
- models/pascal_voc/VGG16/faster_rcnn_end2end/train.prototxt


训练命令：
train cmd:
    experiments/scripts/faster_rcnn_end2end_lightning.sh