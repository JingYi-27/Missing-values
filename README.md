# Missing Values
https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package

This my first data project, I did it for my Data Scientist training. At the beginning the objective was to use all the classification models and to obtain a good score. I thought that I need to do some simple prreprocessing, and the fancy models would give me a magic score. In reality, the calculation ran endlessly, after a long wait, the score didn't change...

I started thinking about data cleaning and features selection seriously. 

This is the main content of this repository:
Missing Data Values
   How to handle them?
   Maybe in some cases, we don't need to do it?
 
I started my research with the simplest model: linear regression, with a single variable y = ax+b. Therefore, the comparison results can be clearly presented in the two-dimensional coordinate system.  
Create a scatter plot (50 points)   
![image](https://raw.githubusercontent.com/JingYi-27/Missing-values/main/images/nuage_de_points.PNG)  
Then I randomly generate some missing values (15 points, 30%), I tried to fill these missing values by mean value and median value. Just to see the impact if we chose a bad filling value, I also added max and min value.  
Distribution after filling:  
![image](https://raw.githubusercontent.com/JingYi-27/Missing-values/main/images/distribution_after_filling.PNG) 

**Linear Regression result comparaison:**  
initial : the initial dataset (50 points without missing values)  
dropna : Missing values are deleted directly (35 points left)

As we can be seen in the figure below:  
1. dropna is pretty close to initial straight line.  
2. max and min results are very inaccurate.  
3. mean and median : they differ from the initial result, but the trend is acceptable.   
   As the amount of data increases (100 points), the result gap decreases.  
![image](https://raw.githubusercontent.com/JingYi-27/Missing-values/main/images/LinearRegression_result_comparaison.PNG) 
![image](https://raw.githubusercontent.com/JingYi-27/Missing-values/main/images/LinearRegression_result_comparaison_100p.PNG) 

