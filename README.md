# Kaggle Mercari Price Suggestion Challenge
A brief solution for [Kaggle Mercari Price Suggestion Challenge](https://www.kaggle.com/c/mercari-price-suggestion-challenge)

## Requirements
- docker >= 17.03

## Getting started
### Build docker image 
```
docker build -t <image name> .
docker run -it -p 8888:8888 --name <container name> <image name>
```

### Setup kaggle api credential
Download kaggle.json and place in the location: ~/.kaggle/kaggle.json.

See details: https://github.com/Kaggle/kaggle-api


### Download and unzip datasets from competition page
Data donwload from the kaggle competition page with kaggle api command.
```
mkdir $HOME/input
cd ./input
kaggle competitions download -c mercari-price-suggestion
unzip '*.zip'
```

### Run jupyter lab
```
jupyter lab --ip 0.0.0.0 --allow-root
```

## What you learn from this kernel
- Manage pipelines for feature engineering by using make_pipeline and FunctionTransformer
- Vectorize short text features
- Train models with multiprocessing.ThreadPool

Details are in a [notebook](https://github.com/tkazusa/Kaggle-Mercari-Price-Suggestion-Challenge/blob/rindoku/notebooks/solution.ipynb).

## References
- [Kaggleは凄かった! 更に簡単な出品を目指して商品の値段推定精度を改善中](https://tech.mercari.com/entry/2018/11/14/172509)
- [1st solution kernel: Mercari Golf: 0.3875 CV in 75 LOC, 1900 s](https://www.kaggle.com/lopuhin/mercari-golf-0-3875-cv-in-75-loc-1900-s)
- [1st solution presentation](https://github.com/pjankiewicz/mercari-solution/blob/master/presentation/build/yandex.pdf)
- [Mercari Interactive EDA + Topic Modeling](https://www.kaggle.com/c/mercari-price-suggestion-challenge/kernels)
