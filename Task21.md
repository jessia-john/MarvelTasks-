# Introduction to Machine Learning (ML)
---
## Machine Learning 
Machine Learning is the process of training a computer with large amounts of data so that it can learn patterns and use them to make predictions or decisions on data it has'nt seen before.
---
I watched the given refernce video and below is my learnings: 

[A Gentle Introduction to Machine Learning - StatQuest](https://www.youtube.com/watch?feature=shared&v=Gv9_4yMHFhI)
<br>StatQuest mentions that Machine Learning is all about presictions and classificatios.

The video uses the question "Will you love StatQuest?" tree to shown how choices lead to classification. Thus, Decision Trees is a simple method to classify data. 

The data we that we give intially which builds is known as **training data**.
To test our model we provide it with some other data the model has'nt seen. This data is known as **testing data**. The accuracy of the model is measured by how well it performs with test data.

![sqiuiggle](https://raw.github.com/jessia-john/Marvel/d7ae5796efb308713bd4bb4d1c19000c1493e0a2/IMG_0115.jpeg)

In the video, We see the green squiggle which performed well with the training data but when we intoduced the testing data set we see how the sum of distance between real and predicted values was larger for it than for the black line.

> Machine learning is essentially the process of choosing the best model (whether a simple line or a complex neural network) that fits specific needs.
> Thus a fancy or complex method doesnt always assure an accurate model. The accuracy in making the predictions is what matters.

---
[How is data prepared for machine learning? - AltexSoft](https://www.youtube.com/watch?v=P8ERBy91Y90)
<br>The second video was about **data preparation**, what it is and how is it done.
## Data preparation 
Data preparation in machine learning is the essential process of cleaning, transforming, and organizing raw data into a structured format suitable for training models, ensuring high-quality input to improve accuracy. 
---
The video showed an example of how collection of wrong data led to the model making wrong predictions, with the example of amazon's hiring automation system.
The data given to the model(training data) consistied of past 10 years resumes and these were male dominated. Thus it penalised resumes mentioning "female" thus leading to unfair elimination. This led to Amazon shutting down this ML recruiting tool.
> Garbage in Garbage out

Thus quality of the tarining data is extremely important for a reliable, fair and accurate model.

**Steps for Data preparation**
1. Defining the problem we need to solve
2. Collecting as much data as we can
    - No one-size-fits-all for dataset size: collect as much relevant data as possible.
      - Examples - Gmail smart reply system- trained with about 238 milion messages.
    - Sometimes lesser quantity of data can also give us the an accurate model 
      - Example: A professor at Tamkang University used ~630 samples to predict concrete compressive strength.
    - It should depend on the complexity anf the algorithm you choose.

3. Quality of data
- Accuracy depends on correctness and domain relevance of data.
    - Domain-mismatch example: using Canadian Thanksgiving sales to predict U.S. Thanksgiving turkey demand would be inadequate.

4. Labeling & features (supervised learning)
- This provide “correct answers” so the model can learn (manual labeling or use existing labels).

5. Data reduction & cleansing
     - Earlier it was mentioned more the data the better but sometimes their will be irrelevant, redundant features that need not be present and it is best to remove such data. The technical term for this is Feature Scaling.
     - Cleaning: Cleaning means refining our data and filling missing values with known/constant or blank values.

6. Feature Scaling
    Standardizing or normalizing file formats and scaling the features using numbers to a commonn range to prevent domination by the features that contain larger value.

Thus these videos gave an understanding into ML and its important step- Data Preparation.




