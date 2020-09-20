# titanic_keras

## 目的
藉由乘客的年齡、性別等因素，來得出每位乘客的存活率。最後再將生存機率和實際結果對比來確認模型的準確性。

## 採用資料集
titanic3.xls 鐵達尼號乘客數據集

## 使用模型
Multilayer perceptron
* Input layer with 9 input dimension (9 features)
* Hidden layers:
  * 40 neurons
  * 30 neurons
  * 60 neurons
  * 60 neurons
* Output layer with 1 output dimension (Dead or survive)


~~~js
model = Sequential()
model.add(Dense(input_dim = 9, units = 40, activation = "relu", kernel_initializer = "uniform"))
model.add(Dropout(0.1))
model.add(Dense(units = 30, kernel_initializer = "uniform", activation = "relu"))
model.add(Dropout(0.1))
model.add(Dense(units = 60, kernel_initializer = "uniform", activation = "relu"))
model.add(Dropout(0.1))
model.add(Dense(units = 60, kernel_initializer = "uniform", activation = "relu"))
model.add(Dropout(0.1))
model.add(Dense(units = 1, kernel_initializer = "uniform", activation = "sigmoid"))
~~~

## Result
MLP學習的結果不論是訓練還是測試其準確率皆為約80%，原則上只要增加模型的複雜度應能使之有所進步。
不過此問題是機率預測而非單純的classifier，此結果已能給出不錯的預測。


