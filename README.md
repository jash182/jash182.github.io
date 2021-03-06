# Projects Overview
The porpuse of this portfolio is to showcase my past experiances in data science. 
The follow are organized in section.

1. R Programming
2. Microsoft Access
3. Python
4. SQL 

# R Programming



### New Zealand Weather

**Introduction**

The following is an analysis of the weatherData data set. The weatherData data set contains data on the recorded weather variables for a number of cities including Chicago, Beijing, and Auckland to name a few. All of the data in the data set being used is from the year 2016. All temperature in this analysis is in Fahrenheit. This analysis focuses on the temperature data of the city of Auckland New Zealand. Auckland has a population of close to 1.5 million and is located on the Northern side of the Island. Both the low and average temperatures are visualized to gain an understanding of the weather patterns of Auckland. New Zealand is in the temperate maritime zone and experiences seasonal changes. This means it has a climate typical of the pacific islands without spending extended periods of time in extreme temperatures. It is expected that Auckland falls into a temperate climate, but New Zealand’s diverse landscape could show a variance in comparison to the rest of the Island.

**Visualization**

![Picture1](https://user-images.githubusercontent.com/82967749/128940098-27b19bbc-e0ee-4a42-8b25-7aecd7b5b2f1.png)


Below is a histogram of the lowest temperatures of Auckland. The X-axis is the recording of the lowest temperatures in Auckland for the year 2016.


![Picture2](https://user-images.githubusercontent.com/82967749/128941013-5e96e16a-eb06-407c-a8fb-4c635c2c6037.png)

**Analysis**

The average temperature shown in the first visualization is a range from 56 degrees to 65 degrees. The Temperature lows of Auckland are on average 50 degrees. This is a moderate temperature in comparison to North American climates. An analysis of the temperature data for Auckland New Zealand suggests Auckland has a relatively cool climate in comparison to the Southern United States but warm compared to Canada. There are no large swings in temperature in Auckland that are not common for seasonal variance. The histogram shows that the average temperature for Auckland NZ in 2016 was between 50- and 60-degrees Fahrenheit. The lowest percentage of days with similarly recorded temperatures were on both ends of the X-Axis. The lowest recorded temperatures were at 20 degrees Fahrenheit and the highest average temperature recorded was 69 degrees Fahrenheit. We produced a 95% confidence interval on Auckland NZ of 60.1 - 61.1. All of the data suggest that Auckland has a seasonal variance of 50 degrees Fahrenheit. Also, these changes in temperature are common for a pacific island in the southern hemisphere. the most common temperature for Auckland is 50 degrees Fahrenheit. For the majority of the year, Auckland is above freezing and never reaches high enough temperatures for a high increase in the chances of heatstroke.

**Conclusion**

To conclude the analysis of the weatherData collected in Auckland New Zealand. There is moderate temperature. The average low temperature is on average 50 degrees Fahrenheit. The average temperature is 60 degrees Fahrenheit. The result of the analysis point to a conclusion that Auckland has temperate temperatures with seasonal variance. For the year 2016, there was only a small proportion of days where the temperature was below freezing. The majority of days experienced cool temperatures below 70 degrees. The results of this analysis can potentially be used for weather predictions and vacation planning.

## Tumor Data

**Introduction**

Our goal was to create two different models looking at the brca data set. The brca data looks at tumors. The models needed to predict if a tumor was benign or malignant. The models produce scores for three metrics accuracy, sensitivity, and specificity.  One model needed a 90% score on at least one metric and one model needed at least 90% score on all three metrics.

Model 1 Visualization
The visualization below looks at the x.radius_mean of tumors.

![Picture3](https://user-images.githubusercontent.com/82967749/128944059-fbf5f1f4-dd4c-4f16-ab82-de527a217525.png)



The table below shows the three metrics that the model was evaluated on. It under performed in accuracy and sensitivity and performed well in specificity. Model 1 looked to see if the looked x.radius_mean was less than 35 and if x.texture_mean was less than 19. Model 1 can predict all benign tumors but is inaccurate in predicting malignant tumors.
      Actual
Predict   B   M
      0 357 140
      1   0  72
      Metric Value
1    Accuracy 0.754
2 Sensitivity 0.340
3 Specificity 1.000


**Model 2 Visualization**

Model 2 looks at the x.radius_mean and x.compactness_worst in its prediction. 

![Picture4](https://user-images.githubusercontent.com/82967749/128944152-4f509757-6e03-4db8-8b33-9010bf6f27e6.png)


**Model 2 Results**
The Model 2 looked to see if x.compactness_worst is less than .375 and if x.radius_mean is less than 15. This allowed Model 2 to have above 90% in all three metrics.
       Actual
Predict   B   M
      B 331  21
      M  26 191
       Metric Value
1    Accuracy 0.917
2 Sensitivity 0.901
3 Specificity 0.927

**Conclusion**
We created two models that predicted if a tumor is benign or malignant. Using the x.radius_mean and x.compactness_worst allowed us to create a more accurate model. Model 2 performs better than model one in predicting if a tumor is benign or malignant.


# MICROSOFT ACCESS

SELECT SKU, SKU_Description, WarehouseID
FROM INVENTORY
WHERE QuantityOnHand > 0
ORDER BY WarehouseID DESC , SKU;

![Access](https://user-images.githubusercontent.com/82967749/129115150-57e81ed7-c294-40f3-9a5c-2c0c79494263.PNG)



# Python

from tkinter import *
window = Tk()
#I set the color to red and gave it a title
window.configure(background = 'red')
window.title('Dog Food')



#This is my elis statments. This takes the dogs weight and places it into categories. 
def multiply():
    num1 = eval(conOFentFirst.get())
    if num1 > 0 and num1 <= 14:
        num2 = 1
        product = 1
        conOFentResult.set("   " + str(product))
        
    elif num1 >= 15  and num1 <= 35:
        num1 = eval(conOFentFirst.get())
        num2 = 3
        product = 3
        conOFentResult.set("   " + str(product))
        
    elif num1 >= 36  and num1 <= 100:
        num1 = eval(conOFentFirst.get())
        num2 = 3
        product = 5
        conOFentResult.set("   " + str(product))
        
  
    else:
        num1 = eval(conOFentFirst.get())
        num2 = 2
        product = "Error"
        conOFentResult.set(" " + str(product))
        
        
    
        


#diffrent photo added
photo = PhotoImage(file = "PawPic.png")
photoimage = photo.subsample(2, 2) 
label = Button(window, image = photo) 
label.grid(row=0, column=4,rowspan = 4,  padx=5, pady=5)

#Here are the lables directing the user
Label(window, text="Dog \nWeight", bg='red').grid(row=0, column= 0, padx=1, pady=5)
Label(window, text="Cups of \nFood ", bg='red').grid(row=0, column=2, padx=1, pady=5)


conOFentFirst = StringVar()
entFirst = Entry(window, width= 10, textvariable=conOFentFirst)
entFirst.grid(row=1, column=0)

conOFentSecond = StringVar()
entSecond = Entry(window, width= 5, textvariable=conOFentSecond)
entSecond.grid(row=1, column=2)
#I changed that claculator button to white and added text
btnMultiply = Button(window, text='Calc', width=7, command=multiply, bg='white' )
btnMultiply.grid(row=2, column=0, padx=15, pady=5)



conOFentResult = StringVar()
entResult = Entry(window, state="readonly", width= 10,textvariable=conOFentResult)
entResult.grid(row= 1, column=2, columnspan=1, padx=20, pady=5)





window.mainloop()


![PythonDF](https://user-images.githubusercontent.com/82967749/129114851-fb9fa704-b750-46f0-b965-75cbce32792d.PNG)



## SQL 

![SQLScript](https://user-images.githubusercontent.com/82967749/129127887-9b840e95-1c4f-4eb2-a24c-128d5ff507e8.PNG)

```

