
![movies-film-cinema-movie-theater-27668457](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/d90ad02c-80fc-446a-a207-17b5497f6b72)


<!DOCTYPE html>  
<html>  
 <body>  
      <h1>Let's Go To The Movies Project</h1> 
 <body>  
</html>

The project will focus on comparing and contrasting specific variable relative to a sizeable movie dataset. 
They actually study "movies"? Yes... Yes they do! 
There is movie analysis beyond the movie-goer experience. In this study, I will focus on reviewing some of the movie elements. 
I will evaluate the following variables:
Movie Rank, Genre, Year, Runtime, Rating, Votes, Revenue and Metascore

<!DOCTYPE html>  
<html>  
 <body>  
      <h2>Reason for this Research</h2> 
 <body>  
</html>

    This is a requirement for Phase I of the Data Science Fellowship completion. 
    
![Data Sciecne Process](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/00d5d352-34c5-46e8-a4b5-79e896eb6573)

EDA and the Data Science Process
Data Science is an all encompassing area of science derived from various elements in the study of Science and Technology. When understanding
Exploratory Data Analysis (EDA) this is a part of the Data Science process. In the most simplistic terms, it involves, exploration of data and the analysis of the data. 
For the purposes of this project, the EDA consists of: Obtainding a viable dataset, Reviewing the dataset, Cleaning the dataset, Analyzing the data for the appropriate model, Fitting the model to the data and a final analysis--- How well did we do? And what are the Next Steps? in the evolution of this project and the overall Data Science process.

<!DOCTYPE html>  
<html>  
 <body>  
      <h2>EDA: Exploratory Data Analysis</h2> 
 <body>  
</html>

![hypothesis-2](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/c7f7059d-4aa9-4e54-aa3b-21cd405b46fd)


<!DOCTYPE html>  
<html>  
 <body>  
      <h3>Hypotheseis (TBD)</h3> 
 <body>  
</html>

<!DOCTYPE html>  
<html>  
 <body>  
      <h3>Research</h3> 
 <body>  
</html>

Research Goals
> Goal 1: Comparative Analysis of specific variables and how they interrelate and effect one another.
>
Variables
> The Attributes for analysis are: Movie Rank, Genre, Year, Runtime, Rating, Votes, Revenue and Metascore
> 
> Goal 2: TBD


#1. DATA

The data is being furnished by an authored contributor and researcher,Promptcloud from Kaggle. This dataset represents a 10-year history of movies between the years 2006-2016.
The location being accessed is: https://www.kaggle.com/datasets/PromptCloudHQ/imdb-data?select=IMDB-Movie-Data.csv
Note: The following if for additional information purposes: Several data sources have made this informaiton possible, they are: IMDB: https://www.imdb.com/  and
The Numbers: https://www.the-numbers.com/

#2. METHOD

The primary objective is the begin with clean data. Then place that data into a predictive model. 
1. Linear Regression Model

#3. CLEANING REPORT
Can be found in the respective Transform notebook.

The purpose of this is to present the data in the most unencumbered manner psossible. The data has been cleared of duplicate rows, and columns, NAN, Non-NaN, and Blanks.

#4. EDA

The EDA Analysis Report will be displayed in the following:

![Regular-Axes3D](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/4f736406-6fc4-4bb7-a399-d8e05cba05af)

![Axes3D-scatter](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/8a046ff0-ff28-4bc2-a4af-5d90e03ba1a2)

![Boxplot](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/2e4a52dc-af1a-40b2-8ef7-019b433c3e98)

![Hexbin](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/4c878f77-e808-4200-9696-54629df0b1a5)

![scatter-matrix](https://github.com/deebaby001/LetsGoToTheMovies/assets/14750340/03aed337-0414-463a-9677-57ed006fe8db)


#5. MODELING

#MODEL using Linear Regression

# Load the Iris dataset
iris = load_iris()
df = pd.DataFrame(data=iris.data, columns=iris.feature_names)

# Define the feature set 'X' and the target variable 'y'
X = df  # All columns in the DataFrame are used as features
y = iris.target  # The target variable is the Iris species

# Assuming that 'X' is your feature set and 'y' is the target variable
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=0)

# Create a Linear Regression object
regressor = LinearRegression()

# Fit the model to the training data
regressor.fit(X_train, y_train)

# Use the model to predict the test set results
y_pred = regressor.predict(X_test)

# Calculate and print metrics
print('Coefficients:', regressor.coef_)
print('Intercept:', regressor.intercept_)
print('Mean squared error (MSE): %.2f'
      % mean_squared_error(y_test, y_pred))
print('Coefficient of determination (R^2): %.2f'
      % r2_score(y_test, y_pred))

##OVERALL ANALYSIS
Based on the data calculations, here's an overall analysis of the
Linear Regression Model:

1. Coefficients: The coefficients of this model are `-0.10627533`, `-0.0397204`, `0.22894234`, and `0.61123074`. These values represent the change in the target variable for a one-unit change in the corresponding feature. With the understanding that all other features remain constant.The signs of the coefficients (-) or (+), indicate the direction of the relationship with the target variable, as referenced.

2. Intercept: The intercept of your model is `0.16149541375178778`. This is the expected value of the target variable in the understanding that  all features are zero. Yet, the interpretation of the intercept often doesn't make sense in the reality, if zero is not a valid value for all or even some of the features.

3. Mean Squared Error (MSE): The MSE of the model is `0.05`. This is a measure of the average squared difference between the actual and predicted values. Therefore, the closer this value is to zero, the better the performance of the model. Nonetheless, in regards to the scale of the MSE, this depends on the scale of the target variable, so it can sometimes be hard to interpret this by its' self.

4. Coefficient of Determination (R^2): The R^2 of your model is `0.91` (or 91% when expressed as a percentage). Thus, 91% of the variability in the target variable can be more easily explained by the features. An R^2 value close to 1 indicates that the model explains a large portion of the variance in the target variable. Therefore, suggesting that the model is performing very well. This is definitely a Good Thing!

#7. FURTHER RESEARCH

In consideration of other prospective areas of research and analysis in consideration of movie data, I think that there is an opportunity to evaluate some of the following areas of interest: Uncover interesting facts about the film making process, Detecting the roles that the movie goer's plays in the film making process, Evaluationg how human nature impacts the movie experience and Evaluating how world events are significant in the script creation and movie development process. 

#8. CREDITS
The data that was accessed for this project is located at the following sites: Target Movie Dataset: https://www.kaggle.com/datasets/PromptCloudHQ/imdb-data?select=IMDB-Movie-Data.csv Supporting Resource Sites: IMDB: https://www.imdb.com/ and The Numbers.com:https://www.the-numbers.com/ have provided additional reference matterials for the purposes of this project.
"Special Thank You" to staff at The Numbers for assisting with additional analytical data and support for this project.











