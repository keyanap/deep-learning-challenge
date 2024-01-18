# deep-learning-challenge

OVERVIEW

The objective of this challenege was to create a model that used machine learning and neural networks to predict the likelihood of sucess of applicants if they were to be funded by the Alphabet Soup Foundation.

RESULTS

    Data Processing 

        Process
            - I loaded my dependicies
            - Loaded the given CSV file was read into a Pandas DataFrame
            - Dropped the non-beneficial columns
            - Found the number of data-points for each unique value for 'APPLICATION_TYPE' and 'CLASSIFICATION'
            - Chose cut off points for binning, then placed low number values into another value named 'Other'
            - Used pd.get_dummies to convert categorical data into numeric data
            - Divided the data into target ("IS_SUCCESSFUL") and features
            - Used train_test_split to creating testing and training dataset
            - Used StandardScaler to scale the training and testing sets

        What variable(s) are the target(s) for your model?
            - The target of this model was is the 'IS_SUCCESSFUL' column. Which is used to determine whether the applicant is successful if funded.

        What variable(s) are the features for your model?
            - The variables that are the features of my model are the remaining columns, after "EIN", "NAME", "ASK_AMT", "SPECIAL_CONSIDERATIONS" columns are removed. 

        What variable(s) should be removed from the input data because they are neither targets nor features?
            - The "EIN", "NAME", "ASK_AMT", "SPECIAL_CONSIDERATIONS" are variables that should be removed as the neither targets or features. They contain information that is not valueable to the model as it cannot help better predict the likelihood of success of applicants. 

    Compiling, Training, and Evalulating the Model

    How many neurons, layers, and activation functions did you select for your neural network model, and why?
        - For my first two attempts in my optimization file, I used two hidden layers. For the second attempt, I changed the number of neurons from 8 & 5 to 8 & 8, respectfully. For my third attempt I added a third hidden layer, for that layer I increased the first layer's neurons to 9, the second layer's was decreased to 7, and the third level was at 3. The activation functions were all 'relu'. I decided to use this activation function as I felt it would handle the data wwere it to get more complex during opitimization.

    Were you able to achieve the target model performance?
        - I was not able to achieve the target model performance of an accuracy of 75%. The loss level for the model was 54.90% in the highest accuracy of 73.54%. That means there was still room to improve the opitimization of the model through preprocessing and training the model.

    What steps did you take in your attempts to increase model performance?
        - I altered the number of neurons and layers. I found that increasing the number of neurons and layers did not improve the accuracy rate, it lowered it. 

SUMMARY

I made three attempts using my model but, I was unable to optimize the model to achieve an accuracy of 75%. The highest I was able to achieve was 73.54%. The model's loss level is at 54.90%, meaning that it still has plenty of room to optimize. I removed two columns, I believe that the 'AFFILIATION' column could possibly be removed to improve the accuracy. I found that with the higher number of neurons that the accuracy decreased so I would keep the number of neurons low. In future attempts, I would utilize other activation functions, keep the number of neurons lower where possible and further clean the data in preprocessing to ensure that it's only data that is beneficial being used. 