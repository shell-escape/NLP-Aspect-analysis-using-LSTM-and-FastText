# Aspect analysis using LSTM and FastText

If you want to read this notebook, please open it in [google colab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true) (you can use hyperlinks on functions and classes there)  
You can also open it in [nbviewer](https://nbviewer.jupyter.org) if you have a intermittent GitHub jupyter notebooks error "Sorry, something went wrong. Reload?"

### The LSTM model is used to predict the aspect ('Comfort', 'Reliability', etc. ) of words in car reviews. XML files with training and test samples are parsed into [BIO_format](https://en.wikipedia.org/wiki/Inside–outside–beginning_(tagging)). [FastText embeddings pretrained on Taiga corpus](https://rusvectores.org/ru/models/) are used. The aspects (classes) are not balanced, so the loss function is weighted. The result expectedly is not very good for aspects with very small words (There are only 60 words in B-Safety and 49 words in I-Safety for example). Because lack of data the model often cusfuses B- and I- (beginning and inside words).

### The data: [Car reviews](https://github.com/Samsung-IT-Academy/stepik-dl-nlp/tree/master/datasets/sentirueval2015) containing 2331 sentences in train and 1986 in test samples.

### Result:
![ConfMatrixAspects](https://user-images.githubusercontent.com/77696343/105871722-a63eb900-600a-11eb-8672-5d6807cdaa2d.png)
