# DSSLIC
Pytorch implmementation of DSSLIC: Deep Semantic Segmentation-based Layered Image Compression

Paper: https://arxiv.org/abs/1806.03348

## Training
# ADE20K Dataset
python3 train.py --name ADE20K_model --dataroot ./datasets/ADE20K/ --label_nc 151 --loadSize 256 --resize_or_crop resize --batchSize 8
# Cityscapes Dataset
python3 train.py --name cityscapes_model --dataroot ./datasets/cityscapes/ --label_nc 35 --loadSize 1024 --resize_or_crop scale_width --batchSize 2

## Testing
# ADE20K testset
python3 test.py --name ADE20K_model --dataroot ./datasets/ADE20K/ --label_nc 151 --resize_or_crop none --batchSize 1 --how_many 50
# Kodak testset
python3 test.py --name ADE20K_model --dataroot ./datasets/Kodak/ --label_nc 151 --resize_or_crop none --batchSize 1 --how_many 24
# Cityscapes testset
python3 test.py --name Cityscapes_model --dataroot ./datasets/cityscapes/ --label_nc 35 --loadSize 1024 --resize_or_crop scale_width --batchSize 1 --how_many 50
