# low-light-image-enhancement
This is a Tensorflow implementation. We decompose the low illumination image into illumination map and reflection map. 
The idea of attention is added to the reflection part, so that when processing the reflection map, attention can be used where it needs to be enhanced more.
## Requirements ##
1. Python
2. Tensorflow 1.4.0
3. numpy, PIL
## Test ##
First download the pre-trained checkpoints from BaiduNetdisk: https://pan.baidu.com/s/1d8gIj-qb6zx23KVDagQcJg ，and The extraction code is 1234,and just run
evaluate_LOLdataset.py

We test some of the images on LOL dataset and share the test results on BaiduNetdisk:https://pan.baidu.com/s/1b47PEQpLURwBeYM5QwYWfQ(low light images),
https://pan.baidu.com/s/1_9Gvat7Rhtna6Ov9T3XPhA(enhanced images),The extraction code is 1234.
## Train ##
We train in LOLdataset,which can be found on the Internet.Save training pairs of LOL dataset under './LOLdataset/our485/' and save evaluating pairs under './LOLdataset/eval15/'. For training, just run
python decomposition_net_train.py
python adjustment_net_train.py
python reflectance_restoration_net_train.py

It's worth noting that if our approach has inspired you, please remember to like it and refer to our address.

