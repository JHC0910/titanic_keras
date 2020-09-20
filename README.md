# titanic_keras

## 採用資料集
titanic3.xls 鐵達尼號乘客數據集

## 使用模型
Multilayer perceptron
* Input layer with 9 input dimension (9 variables)
* Hidden layers:
  * 40 neurons
  * 30 neurons
  * 60 neurons
  * 60 neurons
* Output layer with 1 output dimension 


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


