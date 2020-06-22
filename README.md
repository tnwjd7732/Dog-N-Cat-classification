# Dog-N-Cat-classification

## 사용한 데이터

출처: kaggle dog vs cat   
training image: cat 4000장, dog 4000장 사용   
validation image: cat 1000장, dog 1000장 사용   

## test

### 구성 파일
final_model.h5에 training된 모델 저장되어있음(용량제한으로 업로드하지 못했습니다.)   
dogNcat_training.ipynb --> model을 준비된 dataset으로 training하고 final_model.h5로 저장    
dogNcat_predict.ipynb --> final_model.h5를 load해 prediction_set폴더에 있는 이미지들에 대해 dog인지 cat인지 예측   

### test 방법
1. 학습된 모델 final_model.h5 download   
2. dogNcat_predict.ipynb의 local_path2를 prediction을 위한 데이터가 있는 경로로 수정   
```
local_path2 = 'data/prediction_set/'
```
3. dogNcat_predict.ipynb의 경로를 수정하고 실행하면 해당 경로 내의 이미지들에 대해 00.jpg is a cat/dog으로 예측결과가 출력 됨   

* 제 컴퓨터에서는 이와같은 경로로 prediction_set 및 기타 데이터들을 저장해두었습니다.   
```
c/keras/data/prediction_set/1.jpg
                            2.jpg
                            3.jpg...   
                            
            /training_set/cats/cat0.jpg 
                               cat1.jpg...cat3999.jpg
                         /dogs/dog0.jpg
                               dog1.jpg...dog3999.jpg
                               
            /validation_set/cats/cat4000.jpg
                                 cat4001...cat4999.jpg
                           /dogs/dog4000.jpg
                                 dog4001.jpg...dog4999.jpg
            /learning/inception_v3_weights_tf_dim_ordering_tf_kernels_notop.h5 //transfer training에 사용되는 모델

```
