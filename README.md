Dataset information :The two datasets are related to red and white variants of the Portuguese "Vinho Verde" wine.

link - http://archive.ics.uci.edu/ml/datasets/Wine+Quality

White Wine Exploratory Data Analysis - whitewine_eda.ipynb

        DATASET has 4898 observations with 12 different variables. 11 are feature variables and
        1 target variable (quality)
        
        Count plot on quality ( target variable ) - We can see the dataset has values 3,4,5,6,7,8,9.
        We can see we do not have any observations for 1,2 and 10 in our dataset.Count plot shows how 
        our observations are distributed for our quality ratings. It is also noted that there are very 
        few observations for quality rating 3 and 9. And majority of the observations are of average 
        quality ( ratings 5 and 6)
        
        
        OUTLIERS - We can see that the residual_sugar, free_sulphur_dioxide , total_sulphur_dioxide 
        have outliers ( Huge difference between 75 percentile and max value. This could be easily 
        visualised using box plots/scatter plots.)
        
        Residual Sugar - We can see that there are very few outliers and there is one significantly 
        far away ( quality - 6 )
        
        free_sulpur_dioxide - We can see that there is one value which is significantly far away 
        for quality = 3
        
        total_sulpur_dioxide - We can see that there is one value which is significantly far away 
        for quality = 3.
        
        FACTORS THAT AFFECT QUALITY OF WINE - We can see alcohol content is higher for good quality 
        of wines . It can also be noted that the density decreases as the quality of the white wine increases.
        
        It is also observed that pH, volatile acidity, citric acid, sulphates, total sulphur di oxide,
         free sulphur di oxide have flatter values across different quality of wines. 

Red Wine Exploratory Data Analysis - redwine_eda.ipynb

        DATASET has 1599 observations with 12 different variables. 11 are feature variables and 
        1 target variable (quality)

        Count plot on quality ( target variable ) - We can see the dataset has values 3,4,5,6,7,8.
         We can see we do not have any observations for 1 ,2 ,9 and 10 in our dataset. Count plot 
         shows how our observations are distributed for our quality ratings. We can see that we have 
         very few observations for quality rating 3 , 4 and 8. Also majority of the observations are 
         of average quality ( ratings 5 and 6)
        
        OUTLIERS - We can see that the residual_sugar, free_sulphur_dioxide , total_sulphur_dioxide 
        have outliers ( Huge difference between 75 percentile and max value )
        
        chlorides - We can see one outlier significantly far away for quality = 4 . There are few 
        outliers for qulaity - 5, 6 and 7
        
        residual sugar - We can see one outlier significantly far away for quality = 4 . There are 
        few outliers for quality - 5, 6, 7 and 8
        
        free sulphur dioxide - we can see few outliers across all the quality ratings.
        
        total sulphur dioxide - Two observations are significantly far away for quality rating = 7.
        
        FACTORS THAT AFFECT THE QUALITY OF WINE - we can observe that Best quality red wines have 
        high alochol content, sulphates and citric acid. It can also be observed that best quality 
        wines had lesser volatile acidity and lesser density.
        
Models : 

Neural Network for predicting the quality of wine - (1 - 10) 10 classes - Wine_NN_1_10.ipynb

        Accuracy for white wine dataset ( 10 classes for 250 epochs ) - 54.83%

        Accuracy for red wine dataset ( 10 classes for 250 epochs ) - 62.29%
        
        This accuracy is for the test set that has the ratings ( 3, 4, 5, 6, 7, 8, 9 for white wine ) & 
        ( 3, 4 ,5, 6, 7, 8 for red wine ). Moreover, the network hasnt seen observations for quality 
        ratings ( 1, 2 and 10 for white wine ) and (1, 2, 9,10 for red wine).
        
        I think the best way to approach would be to have three categories - Poor, Average and Best . 
        Wine_NN.ipynb has the code for the same.
        
        
Neural Network for predicting the quality of wine - 3 classes ( Poor, Average and Best ) - Wine_NN.ipynb
        
        
        Accuracy for white wine dataset - 76.33% ( for 250 epochs)
        
        
        Accuracy for red wine dataset - 84.42% (for 250 epochs)
