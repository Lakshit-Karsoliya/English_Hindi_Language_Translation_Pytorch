# English to Hindi Language Translation Pytorch Using Seq2Seq with Attention
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)```3.9``` [![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)  ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Language Translation](https://newsimg.giznext.com/mobile/production/news/wp-content/uploads/2022/05/05152137/Easy-Hindi-Typing-1200_675-735x400.png)

### Dataset used [IIT Bombay English-Hindi Translation Dataset](https://www.kaggle.com/datasets/vaibhavkumar11/hindi-english-parallel-corpus)
### [Checkout Pytorch Language Translation Tutorial using seq2seq](https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html)

### Important Points to Consider
* run the notebook entirely on google colab or run it on local system using checkpoint.pth file of google colab on windows causes issue while reading csv file windows misses some rows completly resulting more words in output(hindi) ie different vocab size in colab as compared to windows enviromnent and these vocab size are used as input in model to resolve this issue i created lang.pth so the checkpoint.pth can be used on windows machine open Test.ipynb to see how to use it i use it to demonstrate the translation but it may be used for traning also

* You can use other csv files for traning i tried a comparitively very small size file but result was not good as we have very less data

* you see imports again and again initially these are going to be two seperate files one for data prepration and another for traninga and testing buy finally i combine them both

* You found that pairs serves no purpose here but you can also proceed traning with pairs i go with eng , hin , array 

* I only use 2000 top records for traning but while inililizing encoder i give lang.n_words which is the vocab size of input created from whole dataset this is due to i am proceding it with incremental traning (traning first 2000 record with 30 epochs and 2000 ...) due to limiting computing power if you have enoughh computing tweak the parameter accordingly this creates a checkpoint.pth file around 1.7GB combinig encoder , decoder , and their respective optimizers state dict [download checkpoint.pth used in Test.ipynb](https://drive.google.com/file/d/1WmjtScfaFyzCkYgnRZQrlHHFsuC75w3m/view?usp=sharing)

* result in output of last cell in Test.ipynb is created by loading checkpoint.pth which is created by traning model for 30 epoch on first 2000 records and loss = 0.1 further traning will reduce it as we have lot of data

#### * Pleanse let me know if you create a better version of this code
