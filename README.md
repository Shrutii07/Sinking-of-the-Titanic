# Sinking-of-the-Titanic
The objective is to predict if a passenger survived the sinking of the Titanic or not using Logistic Regression Model

## Model Representation:
![image51](https://user-images.githubusercontent.com/50697244/72220143-a7be5000-3573-11ea-995e-9bf88baf176d.png)

## Data Processing:
![image48](https://user-images.githubusercontent.com/50697244/72220171-f835ad80-3573-11ea-8b3c-c56b768b45f9.png)

## Algorithm:
![image50](https://user-images.githubusercontent.com/50697244/72220181-0edc0480-3574-11ea-8286-f7438d3d1408.png)

## Logistic Regression:
Logistic regression is a technique borrowed by machine learning from the field of statistics.It is the go-to method for binary classification problems (problems with two class values). SInce the given problem required the output as whether a person travelling on the titanic board survives or not i.e. classification ,we have implemented logistic regression algorithm.
Our model consists of a single perceptron(or node) in the output layer and consists of no hidden layers.Firstly, we have converted the raw data of both the given datasets into a processable datasets using pandas. The categorical data were transformed into numeric labels and we applied dummy encoding scheme on the numeric labels.The final processed data was then fed into the neural network. 
Details of how we got the final processed data is given in the flow chart.

## Loss function:
![Screenshot (4)](https://user-images.githubusercontent.com/50697244/72220234-a5102a80-3574-11ea-89b3-fa94eb927fb7.png)

## Optimisation Algorithm:
![Screenshot (7)](https://user-images.githubusercontent.com/50697244/72220512-65970d80-3577-11ea-9cc2-45574563f32a.png)

![image49](https://user-images.githubusercontent.com/50697244/72220280-09cb8500-3575-11ea-8659-071d8ba47b6e.gif)

## How predict function (in code) works:
X axis= z   ,Y axis=sigma(z)

![image52](https://user-images.githubusercontent.com/50697244/72220289-2f588e80-3575-11ea-845e-dc8fc422f16f.png)

This is graph of sigmoid function. From graph it is seen that sigma(z) varies from 0 to 1.
If z -> infinity  , sigma(z)=1 also if z -> -infinity , sigma(z)=0.
What predict function does is:
 if sigma(z)>=0.5 then y=1 and if sigma(z)<0.5 then y=0
Where y is the predicted value for a particular z.

## Model
X : input feature vector in which each column corresponds to a training example’s input features.

Y : Ground truth labels in which each column corresponds to a training example’s ground truth label.

X=(x(1),x(2)........ , x(m))

Y=(y(1),y(2)....... ,y(m))

**1. Initializing Parameters:**

W was initialized to zero column array having 19 rows(number of input features after dummy encoding).
B was initialized to scalar zero. 

**2. Forward Propagation:**

![Screenshot (6)](https://user-images.githubusercontent.com/50697244/72220355-e1905600-3575-11ea-90e5-8286408c090a.png)

**3. Backward Propagation:**

![Screenshot (8)](https://user-images.githubusercontent.com/50697244/72220432-9a569500-3576-11ea-917a-3e02e092342e.png)

**4. Update Parameters:**

W := W - alpha x dW

b := b - alpha x db

Where alpha is the learning rate.

**5. Perceptron:**

For a given number of iterations ,the following steps take place in order:

1. Forward Propagation

2. Backward Propagation

3. Updates of parameters

4. Calculation of cost and accuracy on every 100th iteration.

Finally the model function returns lists of cost and accuracy calculated at every iteration. Using them we plotted two graphs :

Cost vs number of iterations (per 100th iteration)

Accuracy vs number of iterations (per 100th iteration)

## Results:
![image53](https://user-images.githubusercontent.com/50697244/72220485-020ce000-3577-11ea-9b2d-d57e77137586.png)

Since the cost curve is continuously decreasing it is implies that our algorithm is working properly. 
