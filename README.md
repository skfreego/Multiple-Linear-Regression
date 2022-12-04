## Predicting a Startups Profit/Success Rate using Multiple Linear Regression in Python

#### The dataset contains the following features(independent variables): —
……..1)R&D Spend-Total amount of money spent on Research and Development by the startup.
……..2)Administration-Total amount of money spent on Administration by the startup.
……..3)Marketing Spend-Total amount of money spent on Marketing by the startup.
……..4)State-The State or region in which the startup is launched or operates

##### Encoding categorical data
	Importing the Label Encoder Class along with OneHotEncoder

###### Avoiding the Dummy Variable Trap
	The Linear Regression equation would look like —> y=b(0)+b(1)x(1)+b(2)x(2)+b(3)x(3)+b(4)D(1)+b(5)D(2)+b(6)D(3)…b(n+3)D(m-1)
Here D(1)…D(m-1) are the m dummy variable’s which we had defined earlier in LabelEncoder and OneHotEncoder
Well if you are sharp enough you might have noticed that the even though there are m dummy variables we have excluded the last dummy variable D(m)
The reason to that is a concept called Dummy Variable Trap in Machine Learning…and to avoid that we must always exclude the last Dummy Variable
If you are more interested then feel free to research a bit on Dummy Variable Trap!!

Dropping the 1st column out of the Dataset which contains one of the OneHotEncoded values…

X = X[:, 1:]

