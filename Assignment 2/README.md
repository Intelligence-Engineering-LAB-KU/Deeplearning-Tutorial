# 딥러닝 특론 과제 2

## 1. CNN 기반 CIFAR-10 데이터셋 분리 튜토리얼 수행 (50점)

- [링크](https://github.com/Intelligence-Engineering-LAB-KU/Deeplearning-Tutorial/blob/master/Tutorial_4_CIFAR10_CNN.ipynb)에 접속하여 아래그림과 같이 해당 튜토리얼에서 사용하는 모델(5.모델 학습)을 학습 및 성능 테스트(6. 모델 성능테스트) 해보십시오.

![](https://camo.githubusercontent.com/30f397ca3d6671981fd690aa961736f549b1c126/68747470733a2f2f696d6775722e636f6d2f534478484568522e706e67)



## 2. 테스트 성능이 60% 이상 나오는 모델을 만들어보십시오.

- 7번 해보기와 같이, 테스트 성능이 60%이 이상 나오는 모델을 만들어보십시오.

- TODO-LIST 부분을 작성해주신 후, 셀을 수행하세요.

- 다른 부분은 수정하시면 안됩니다. 

  ```python
  tf.random.set_seed(2020)
  
  ##  이 부분을 수정하세요 ## 이 부분을 수정하세요 ## 이 부분을 수정하세요
  my_model = #TODO-LIST
  ## 이 부분을 수정하세요 ## 이 부분을 수정하세요 ## 이 부분을 수정하세요
  
  opt = keras.optimizers.Adam()
  
  my_model.compile(loss='categorical_crossentropy',
                optimizer=opt,
                metrics=['accuracy'])
  
  my_model.fit(norm_x_train, y_train,
            batch_size=32,
            epochs=10,
            validation_data=(norm_x_test, y_test),
            shuffle=True)
  
  scores = my_model.evaluate(norm_x_test, y_test, verbose=1)
  print('Test loss:', scores[0])
  print('Test accuracy:', scores[1])
  ```

  



## 제출 방법 및 양식

- 주피터 노트북을 제출하되, pdf로 인쇄하여 제출 (사용 브라우저에서 인쇄(```Ctrl+P```) 버튼 누른 뒤, ```pdf```로 인쇄)
- google colab을 이용하시면 편하게 작업을 수행하실 수 있습니다. 
  - [링크](https://github.com/Intelligence-Engineering-LAB-KU/Deeplearning-Tutorial/blob/master/Tutorial_4_CIFAR10_CNN.ipynb) 클릭 후 보이는 첫줄의 open in colab을 클릭하시면, 같은 내용의 jupyter notebook을 colab에서 이용하실 수 있습니다.  