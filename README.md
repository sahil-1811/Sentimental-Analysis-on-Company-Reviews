# Sentimental Analysis on Company Reviews
- The goal of this project is to scrape the prominent Job-Hunting website "Indeed.com"
based on the job designation to find mainly the list of companies, user ratings, reviews
and descriptions.
- Categorized the organizations depending on their field and domain, and we will
assess existing employee work satisfaction based on the reviews scraped.
- All employee reviews posted on the job board will be examined in order to derive useful
insights and employee sentiments. This will assist individuals in picking the companies for
which they desire to apply.
- Implemented various EDA techniques ranging from Histogram, Pie charts, Bar plots
and Word Cloud.
- We focused mainly on the library - BeautifulSoup to scrape the reviews of about
150 companies for the two designations, precisely, Data Scientist and
Pharmacist
- The attributes scraped are: company name, designation, title, review, date,
place and ratings
- This scraped data of company reviews was used further to implement
sentiment analysis

## Database Description
- We visited the website https://www.indeed.com/m/ and looked for the top firms in Data Science, and
Pharmacy employment.
- Furthermore, we chose over 150 companies and scraped a list of company names, designation,
overall ratings given to the company by employees for a specific sector, the date on which the review
was posted, job descriptions of the companies that fall within the relevant areas for the positions, top
employee reviews, and the company's location.
![image](https://user-images.githubusercontent.com/68710115/213902261-77f8d7b6-dd48-4d7b-84a1-ee91f62d6c8a.png)

![image](https://user-images.githubusercontent.com/68710115/213902266-06727640-deb2-4aa2-b735-bf540db45514.png)

## Exploratory Data Analysis
![image](https://user-images.githubusercontent.com/68710115/213902288-3b56079f-7ddb-485f-93a8-89590f2e82df.png)

![image](https://user-images.githubusercontent.com/68710115/213902297-6abdc997-bfcb-4065-a8b1-5ba8a02558ab.png)

![image](https://user-images.githubusercontent.com/68710115/213902301-a37bdca0-9afe-4379-b654-781a68c4f0ff.png)

![image](https://user-images.githubusercontent.com/68710115/213902305-7c2c2a18-7ad4-4105-8cfc-3b697e868d43.png)

![image](https://user-images.githubusercontent.com/68710115/213902309-ff210f8a-0b4f-4038-b2dc-934deb4d2021.png)

## Sentimental Analysis
- For the purpose of sentimental analysis, we first started with cleaning out all the
special characters and punctuation marks using regex.
- We further went ahead to remove all the “stopwords” from the text so that it
becomes easier for the system to analyze the text and make the required
predictions.
- Post cleaning our textual reviews, using the TextBlob library provided by Python, we
classified the reviews into positive, negative and neutral.
- TextBlob helps the user by returning a polarity value.
- For our dataset, if the polarity value was less than the sentiment was classified as
negative; if the polarity value was equal to zero, the sentiment was neutral and if the
polarity was a positive value, the sentiment was assumed to be positive.
![image](https://user-images.githubusercontent.com/68710115/213902346-5550c6db-d194-4604-aa1c-31df6c0e7fc8.png)

![image](https://user-images.githubusercontent.com/68710115/213902354-143c35af-0a2d-4ea9-b2f8-bc67ed6c7479.png)

## Machine Learning Algorithms
### Logistic Regression
- Logistic regression is a supervised Machine Learning algorithm commonly used for
classification purposes.
- The Logistic model, using the ‘saga’ solver and 1000 iterations gave us an accuracy of
80%.
![image](https://user-images.githubusercontent.com/68710115/213902405-5a6e1e28-a659-40a1-a851-a714617df0a5.png)

### Multinomial Naive Bayes
- Multinomial Naive Bayes algorithm is a probabilistic learning method that is mostly used in
Natural Language Processing (NLP).
- With the help of sklearn library, MultinomialNB, which alpha as 1, also gave us an accuracy of
79%.
![image](https://user-images.githubusercontent.com/68710115/213902462-cb438a6a-164a-4481-8dad-9d2f19520f16.png)

### Decision Tree Classifier
- Decision tree algorithm falls under the category of supervised learning. They can be used
to solve both regression and classification problems.
- The intuition behind Decision Trees is that you use the dataset features to create yes/no
questions and continually split the dataset until you isolate all data points belonging to
each class.
- With this process you’re organizing the data in a tree structure.
- In our program we have used a maximum depth of 120 and min_samples_split as 3 to
receive an accuracy of 87%.
![image](https://user-images.githubusercontent.com/68710115/213902473-c44bba1f-e0fa-4b55-a467-c4f753182199.png)

## Conclusion and Comparison
In this project, we have implemented Multinomial Naive Bayes, Decision Tree
Classifier and Logistic Regression. Comparing these three algorithms, we
have got the best accuracy with Decision Tree Classifier and the least
accuracy with Logistic Regression. This is because the decision tree classifier
has helped us in removing the outliers. In addition to that, since our
classification is categorical, the decision tree is bound to give better results
than Logistic Regression. The decision tree also performed feature selection
better than multinomial naive bayes, hence, superseded the accuracy.



