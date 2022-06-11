# Data Collection 2

Was enough data gathered to generate a significant result? 3
- Yes, 18,845 unique titles were scraped.
Was data collected that was useful and relevant to the project? 3
- Yes. The subreddit a post originated from as well as the age of the post was scraped.
Was data collection and storage optimized through custom functions, pipelines, and/or automation? 1
- You copy and pasted your entire scraping pipeline for the first few scrapes and then made a function to do this later on. You should edit the notebook to reflect these improvements and replace your copy pasted sections with your function. This will make your overall project look more professional and display for your reader right away that you know how to create and use custom functions in a productive and pythonic way.
Was thought given to the server receiving the requests such as considering number of requests per second? 2
- It looks like you only made one request per scrape and manually waited before rerunning your later scrapes which technically meets this requirement. For future scraping try automating this into your pipeline using loops and time.sleep() so that you can run your script without having to interact with it until the task has been completed.

# Data Cleaning and EDA 1

Are missing values imputed/handled appropriately? 3
- You only had null values in your post body column and you choose to drop this column. Great work showing your reader this issue and explaining your thought process and logic behind your decision to drop the column.
Are distributions examined and described? 0
- No distributions are examined or described.
Are outliers identified and addressed? 1
- You addressed outliers by removing posts with more than 2000 comments which left you with 99.59% of your posts. You then made another scatter plot and adjusted your outlier threshold to 500. What I was unsure of was why you choose these particular number as your definition for outliers. You mention the scatter plots but while scatter plots can give you a sense of the presence of outliers they can't really be identified using them alone. Consider using a boxplot to help identify outliers which defines outliers as Q3+1.5\*IQR.
Are appropriate summary statistics provided? 1
- You provided a number of summary statistics but did not interpret them and it was unclear what the takeaways were or if you were using them to inform you about your data. You do interpret some summary statistics in your modeling section but I would like to see a bit more interpretation in your EDA.
Are steps taken during data cleaning and EDA framed appropriately? 3
- Good use of markdown to help guide your reader through your data cleaning and EDA steps.
Does the student address whether or not they are likely to be able to answer their problem statement with the provided data given what they've discovered during EDA? 3
- Yes

# Preprocessing and Modeling 2

Is text data successfully converted to a matrix representation? 1
- Make sure that when you use tfidf vectorizer you fit only on your training set and not your entire corpus.
Are methods such as stop words, stemming, and lemmatization explored? 3
- Stop words are removed and stemming and lemmatization are explored.
Does the student properly split and/or sample the data for validation/training purposes? 3
- Yes
Does the student test and evaluate a variety of models to identify a production algorithm (AT MINIMUM: two models)? 3
- KNN and random forests are used to create models with both stemmed and lemmatized text.
Does the student defend their choice of production model relevant to the data at hand and the problem? 3
- Yes.
Does the student explain how the model works and evaluate its performance successes/downfalls? 1
- You mentioned the sensitivity and specificity as well as the accuracy of your model in your modeling section but you didn't really evaluate whether you considered where these numbers were at a success or downfall of your model. Try to elaborate a bit more on what the positives and negatives are of your choosen model vs the others relative to the data at hand.

# Evaluation and Conceptual Understanding 2

Does the student accurately identify and explain the baseline score? 3
- Yes.
Does the student select and use metrics relevant to the problem objective? 2
- Accuracy, sensitivity, specificity, and standard deviations of cross val scores are used. The one thing you could elaborate a bit more on which of these metrics are more or less important to your problem. Do you care more about false positives or false negatives for this task and why?
Does the student interpret the results of their model for purposes of inference? 3
- Yes
Is domain knowledge demonstrated when interpreting results? 3
- Yes
Does the student provide appropriate interpretation with regards to descriptive and inferential statistics? 1
- You interpreted some summary statistics in your modeling section but in your EDA notebook the statistics you displayed often lacked an interpretation. Make sure when you display statistics you let your reader know how they are informing you about your data and what the takeaways are.

# Conclusion and Recommendations 2

Does the student provide appropriate context to connect individual steps back to the overall project? 3
- Great work using a lot of markdown to help guide your reader through your project.
Is it clear how the final recommendations were reached? 3
- Good job specifying which model you were pulling your feature importances from and bringing specific numbers into your conclussions rather than speaking broadly about your data.
Are the conclusions/recommendations clearly stated? 3
- Yes.
Does the conclusion answer the original problem statement? 3
- Yes
Does the student address how findings of this research can be applied for the benefit of stakeholders? 2
- This is the one area you could elaborate a bit more on. You did recommend some posting guidlines but you could elaborate a bit more and how these could be applied for the benefit of stakeholders.
Are future steps to move the project forward identified? 3
- Yes

# Project Organization 3

Are modules imported correctly (using appropriate aliases)? 3
- Yes
Are data imported/saved using relative paths? 3
- Yes
Does the README provide a good executive summary of the project? 3
- Great work writing an informative summary that gives your reader a great overview of your project.
Is markdown formatting used appropriately to structure notebooks? 3
- Great work using a lot of markdown to help guide your reader through your project.
Are there an appropriate amount of comments to support the code? 3
- Good job including comments to support certain areas of your code and provide your sources when you used outside resources.
Are files & directories organized correctly? 3
- Yes
Are there unnecessary files included? 3
- No
Do files and directories have well-structured, appropriate, consistent names? 3
- Yes

# Visualizations 2

Are sufficient visualizations provided? 2
- Good job providing bar and scatter plots to visualize your data. In the future you should try to include more histograms and box plots to help visualize the distributions of your data.
Do plots accurately demonstrate valid relationships? 3
- Yes.
Are plots labeled properly? 3
- Yes
Are plots interpreted appropriately? 3
- Good job interpreting your plots right away and informing your reader of what you are seeing in your visualizations.
Are plots formatted and scaled appropriately for inclusion in a notebook-based technical report? 3
- Great work making your titles larger to match the increased size of your plots.

# Python Syntax and Control Flow 2

Is care taken to write human readable code? 2
- For the most part your code is very readable. The one note I have is to always avoid naming your variables df_tvec1, df_tvec2 and so on. If you are ever just adding and changing a number on the end of your variable names you should change them to be more explicit about what objects they really point to.
Is the code syntactically correct (no runtime errors)? 3
- Yes
Does the code generate desired results (logically correct)? 3
- Yes
Does the code follows general best practices and style guidelines? 1
- You mostly follow best practices and style guidlines but you have some lines that exceed the maximum recommended character length and get cut off when I render them on my screen. Check out https://peps.python.org/pep-0008/ for a detailed python style guide and lets chat about installing notebook extensions to get you a handy red line that will help you here.
Are Pandas functions used appropriately? 3
- Yes
Are sklearn and NLTK methods used appropriately? 3
- Yes
