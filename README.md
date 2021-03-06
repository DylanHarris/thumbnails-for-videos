# Auto selection of thumbnails for videos.

**A thumbnail worth a thousand frames**

Deep Neural Network - Automatic selection of the most optimal and relevant Thumbnails for Videos.

This repo provides the package that can select top 3 most **optimal and most relevant thumbnails** for any given video. Here are a few example outputs:

<img src='imgs/result1.png'>

This package provides - 
- A pretrained model
- Code to run the model on new videos, on either CPU or GPU
- Instructions for training the model

## Luarocks Installation

```bash
luarocks install torch
luarocks install nn
luarocks install image
luarocks install lua-cjson
luarocks install https://raw.githubusercontent.com/qassemoquab/stnbhwd/master/stnbhwd-scm-1.rockspec
luarocks install https://raw.githubusercontent.com/jcjohnson/torch-rnn/master/torch-rnn-scm-1.rockspec

luarocks install cutorch
luarocks install cunn
luarocks install cudnn
```

## PIP Installation

```bash
cv2 - pip install opencv-python
matplotlib.pyplot - pip install matplotlib
PIL - pip install pillow
spacy - pip install -U spacy
spacy - python -m spacy download en
```

## Pretrained model

You can download a pretrained CNN Binary Classifier model by running the following link:

[https://drive.google.com/drive/u/1/folders/1vtrfy1sGQM5SUqdN85LRhr4qXD8Tiu3L]

This will download a zipped version of the CNN model (about 1.5 GB)

You can download a pretrained DenseCap model by running the following script:

sh scripts/download_pretrained_model.sh

This will download a zipped version of the model (about 1.1 GB) to `data/models/densecap/densecap-pretrained-vgg16.t7.zip`, unpack it to `data/models/densecap/densecap-pretrained-vgg16.t7` (about 1.2 GB) and then delete the zipped version.


## Datasets used

1. Open Image Dataset 

[https://github.com/openimages/dataset]


2. Youtube 8M Dataset

[https://research.google.com/youtube8m/]


## Steps to Run the code

1. Clone the thumbnails-for-videos repo.
2. Luarocks Installation
3. PIP Installation
4. Download the CNN model from the link provided in the Pretrained model section
5. Unzip the CNN model and move it to the following folder -  thumbnail/cnn/model/
6. Download the DenseCap model by running the script provided in the Pretrained model section.
7. If there is no error in any of the above steps then the code is ready to generate thumbnails for any video.
8. To generate the thumbnails, run the following code under the thumbnail folder - 
python inference.py [path to the video] [video title or description]
9. The candidate thumbnails will be generated in the following folder - thumbnail/candidate_thumbnail/


## References

1. Dencecap 

**[DenseCap: Fully Convolutional Localization Networks for Dense Captioning](http://cs.stanford.edu/people/karpathy/densecap/)**,
<br>
[Justin Johnson](http://cs.stanford.edu/people/jcjohns/)\*,
[Andrej Karpathy](http://cs.stanford.edu/people/karpathy/)\*,
[Li Fei-Fei](http://vision.stanford.edu/feifeili/),
<br>


2. Spacy

[https://spacy.io/]






