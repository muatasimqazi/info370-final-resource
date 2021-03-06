# Predicting Cardiovascular Disease
## [Final Resource available here](https://muatasimqazi.github.io/info370-final-resource/)
## Project Description
* What is the overarching purpose of your research project, and why is it an important undertaking?

>The overarching purpose of our research project is it study the relationship between different risk factors that can cause cardiovascular disease. We believe it is an important undertaking because we are always looking to understand the relationships between lifestyle and health. With science-backed findings, we want to help individuals in making better decisions, communities in promoting healthier public health practices, and governments in finding the best balance in resource-allocation between public healthcare and research and development.

* How does your research fit into the broader problem domain? You should cite at least 3 papers that help contextualize your research.
> Our research would fit into the broader problem in that the potential to learn from data is always stronger when it is studied more times. As a lot of meta research shows, the conclusions of a study may vary based on statistical methods used, covariates chosen, or even the academic backgrounds of the researchers. 

> For decades now, cardiovascular disease has been the leading killer of Americans. In the past years however, advances in biomedical research has improved emergency response systems and treatment, and public health has been better in prevention efforts. [Source: CVD: A costly burden for America](https://healthmetrics.heart.org/wp-content/uploads/2017/10/Cardiovascular-Disease-A-Costly-Burden.pdf). Even so, cardiovascular disease continues to be the leading cause of death, a major cause of disability, and a major contributor to productivity loss in Americans. In fact, an estimated 71.3 million--about one in three--Americans have one or more types of heart disease. This burden translates not only in the loss of life, but also affects society’s quality of lives and puts a toll on public healthcare spending that could otherwise be put into other social good programs. Prevention is usually much cheaper to invest in than treatment, and so understanding risk factors has a huge potential impact on reducing burden. [Source: An overview of CVD burden in the U.S.](https://www.healthaffairs.org/doi/full/10.1377/hlthaff.26.1.38)

> Understanding risk factors also has a lot of potential in impacting individuals lifestyle choices. The more people understand about what behaviors could increase their chances of contracting heart disease, the more informed their choices are going to be. When we look at commonly cited risk factors for heart disease, it seems that smoking is the one that has seen the most change due to the push for prevention against lung cancer. This type of advocacy is something that could be pushed better in both public health and medicine, and particularly for factors that the American public has not been very adamant about (for example, a lot of Americans live very sedentary lifestyles, and a lot of Americans do not consume enough fruit, vegetables, and/or grains). Another domain of research to take into consideration would be looking into possible socioeconomic barriers that prevent people from making these lifestyle choices. [Source: Lifestyle and the cardiovascular disease](http://www.onlinejacc.org/content/69/9/1126)

> Besides lifestyle choices, it is also important to understand demographic and genetic factors, such as age, race, sex, etcetera that are predisposing people to heart disease. This is important because oftentimes, the burden may fall on people unequally. This suggests that prevention measures may need to be different and especially catered to different individuals. This would help ensure that the burden of heart disease is decreased as much as possible. [Source: Personality, stress, smoking, and genetic predisposition as synergistic risk factors for cancer and coronary heart disease](https://link.springer.com/article/10.1007/BF02691067)

* What specific hypothesis (hypotheses) are you going to test?

    >The **specific hypotheses** that we are going to test are:

    >**Null hypothesis**: There is no relationship between weight, cholesterol, smoking, and alcohol intake and the presence of cardiovascular disease.

    >**Alternative hypothesis**: There is no relationship between weight, cholesterol, smoking, and alcohol intake and the presence of cardiovascular disease.


* What are the datasets you'll be working with to answer this question? Please include relevant background describing the datasets you identify.

>To answer this question, we will be working on a dataset about cardiovascular disease [available on Kaggle](https://www.kaggle.com/sulianova/cardiovascular-disease-dataset) that consists of 70,000 records of patients data. We were particularly interested in exploring a research question in the domain of healthcare. We wanted to understand the relationship between some given risk factors that contribute to a certain disease. The main outcome that we are concerned with is the presence or absence of cardiovascular disease. Our search led us to this dataset and had all the relevant information that we could use to predict cardiovascular disease. 
    
>According to the Center for Disease Control and Prevention, “heart disease is the leading cause of death for both men and women” ([Source: Heart Disease Fact Sheet](https://www.cdc.gov/dhdsp/data_statistics/fact_sheets/fs_heart_disease.htm)). In 2015, more than half of these deaths were men. The main risk factors for cardiovascular disease are high blood pressure, cholesterol, and smoking. CDC also lists some medical conditions, such as diabetes, obesity, as well as lifestyle choices, such as poor diet, physical inactivity, and excessive alcohol use, as common risk factors. Our dataset includes data for most of these risk factors.
The data was collected at the moment of medical examination of about 70,000 individuals. The dataset’s unit of analysis is an individual person, and contains the following features: age, height, weight, gender, systolic blood pressure, diastolic blood pressure, cholesterol, glucose, smoking, alcohol intake, physical activity, and presence or absence of cardiovascular disease.
* What statistical and machine learning methods do you plan on using to test your hypothesis?
>For our models, since we have multiple binary/classification features, we will be using models that are classifier friendly which are logistic regression, decision tree, and k-Nearest Neighbor. Logistic regression, which unlike linear regression, the prediction for the output is transformed using non-linear function called the logistic function. The logistic function will transform value into the range of 0 to 1 and predict a class value. By using logistic regression, we can also fit a linear regression of binary/classification and generate predictions, which can be interpreted as the probability of default. If default probabilities are negative, then we can say the model’s predicted results don’t make sense and vice versa. Moreover, Decision tree which utilizes an if-then rule and rules are learned sequentially using the training data and K-Nearest Neighbor which stores all instances correspond to training data points in n-dimensional space.  For our numeric data, we want to use  Linear SVC or Ensemble classifier we are predicting whether an individual person has cardiovascular disease.

* Who is your target audience for the resource you will build? Depending on the domain of your data, there may be a variety of audiences interested in using the dataset. You should hone in on one of these audiences.

>There could be numerous target audiences for our resource since healthcare topics are of interest to almost everyone. Our resource will be useful for particularly people affiliated with healthcare as well as individuals who want to prevent cardiovascular disease or want to learn more about it. For the former, the resource can provide useful insights as what specific risk factors are of more importance than the others. In addition, the resource can help them predict whether a patient could have cardiovascular disease based on the variables of risk factors we will be exploring as part of this project. For common individuals, the resource can provide useful information on which risk factors to pay heed to based on our outcome of interest.

* What should your audience learn from your resource? Consider specific questions they may want to answer.
>Professionals from the healthcare industry could learn what risks factors are bigger contributors to cardiovascular disease. They could get specific insights from the resource that otherwise would not be possible by just looking at the data of a particular patient. A question that they could get an answer to from our resource would be what specific suggestions they should make to an individual patient based on what the model predicts so that they could get that particular risk factor under control.

# Technical Description
This section of your proposal is an opportunity to think through the specific analytical steps you'll need to complete throughout the project.
 
* What will be the format of your final web resource (Shiny app, HTML page or slideshow compiled with KnitR, etc.)?
>We will use Jupyter notebook to generate an HTML  page as the format of our final web resource and we will also publish our final project on Github.
* Do you anticipate any specific data collection/data management challenges?
>Although this dataset provides us information about individual person’s physical activity status, alcohol intake and whether they smoke or not, these features are rather vague since they are all categorical data instead of continuous data. However, we can use classifier and K-means to interpret the relationship between these binary features and outcome variable. Since we found this dataset on Kaggle, one approach to this is to ask people who posted this dataset on Kaggle to clarify information about these binary columns. Another data management challenge we anticipate is that the unit of  the “age” column in our dataset is in days. We will have to calculate age in years by converting the days to years in order to get a better understanding of how age affects cardiovascular disease. 
* What new technical skills will need to learn in order to complete your project? 
>So far in this class for the notebooks and assignments we have been using the language Python, while it is full of libraries and easy to implement, there exist some limitation when it comes to data visualization with matplotlib. However, the language R and its library ‘ggplot2’ might be a good alternative and space to explore. R’s ‘ggplot2’ allows you to create plots in steps, basically customize your plot and have any kind of styling you want/imagine. In addition, there are also many bunch of libraries that extend ggplot2 making it easy to create all sorts of different types of plots, apply aesthetic looking theme, etc. So if we want to customize and make our visualization more aesthetic, we might need to consider learning R and ggplot2. 
> Another technical skill we will need to learn is dealing with 0/1 outcome and classifier. Even though in class we have done machine learning on the breast cancer data which has 0/1 outcome, but our data has multiple columns with binary data/categorical data such as if someone smokes, drinks alcohol, and/or is active, which the breast cancer data has all continuous data but outcome data, so we do need to explore more on how to use binary features on machine learning and how does that affect/change the methods we have used so far in the class. 
* How will you conduct your analysis? Please include a detailed description of your intended modeling approach. 
>First, we need to clean and modify our data set. We will apply feature selection such as variance threshold and percentile selection to get rid of irrelevant data, which both methods provided by python library. We could possibly drop the id column since it’s not too relevant to the outcome and turn age column from unit of days to years. We would then split 70% of the dataset to be our training data and 30% to be our testing data. Then, using grid search, we will find the optimal set of parameters for creating our models. Then we apply statistical and machine learning methods and algorithms on our training data. After applying our algorithms, we will then validate our training data using testing data. 
* What major challenges do you anticipate? 
>Find a good data set to work with was actually the biggest challenge for us so far, the fact that there are so many data sets out there and deciding whether the data set is applicable for machine learning. Also, dealing with a mix of continuous features and binary/classification features will be challenging as well. We could potentially switch to another data set if we found this dataset too difficult to work with. 

## Works Cited


Asiri, Sidath. “Machine Learning Classifiers.” Towards Data Science. Jun 11, 2018. www.towardsdatascience.com/machine-learning-classifiers-a5cc4e1b0623. Accessed 1 Mar. 2019. 

“Cardiovascular Disease: A Costly Burden for America. Projections Through 2035.” American Heart Association. www.healthmetrics.heart.org/wp-content/uploads/2017/10/Cardiovascular-Disease-A-Costly-Burden.pdf. Accessed 1 Mar. 2019. 

“Choosing the Right Estimator.” SciKit Learn. Jan. 2017. www.scikit-learn.org/stable/tutorial/machine_learning_map/index.html. Accessed 1 Mar. 2019.

Eysenck, H. J. Grossarth-Maticek, R.; Everitt, B. “Personality, Stress, Smoking, and Genetic Predisposition as Synergistic Risk Factors for Cancer and Coronary Heart Disease.” Integrative Physiological and Behavioral Science. https://link.springer.com/article/10.1007/BF02691067. Accessed 1 Mar. 2019

Gaziano, Thomas A. “Lifestyle and the Cardiovascular Disease: More Work to Do.” Journal of the American College of Cardiology. www.healthaffairs.org/doi/10.1377/hlthaff.26.1.38. Accessed 1 Mar. 2019.

“Heart Disease Fact Sheet.” Center for Disease Control and Prevention. 23 Aug. 2017. www.cdc.gov/dhdsp/data_statistics/fact_sheets/fs_heart_disease.htm. Accessed 28 Feb. 2019.

Mensah, George A.; Brown, David W. “An Overview of Cardiovascular Disease Burden in the United States.” Health Affairs. www.healthaffairs.org/doi/10.1377/hlthaff.26.1.38. Accessed 1 Mar. 2019.

