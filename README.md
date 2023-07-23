<html class="" dir="ltr" lang="en">
<script src="https://cdn.cookielaw.org/consent/361df3af-d1f9-49b0-bece-f1622873f2ca/OtAutoBlock.js" type="text/javascript"></script>
<script src="https://cdn.cookielaw.org/consent/361df3af-d1f9-49b0-bece-f1622873f2ca/otSDKStub.js" type="text/javascript" data-domain-script="361df3af-d1f9-49b0-bece-f1622873f2ca"></script>
<script src="https://www.googletagmanager.com/gtag/js?id=G-XXN50SC2TH" async=""></script>
<body class="with-left-side course-menu-expanded with-right-side assignments primary-nav-expanded full-width context-course_3251 responsive_student_grades_page webkit chrome no-touch">
  <h1 class="title">Module 21 Challenge - deep-learning-challenge </h1>
  <h3>Background</h3>
  <p>The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.</p>
  <p>From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:</p>
  <ul>
    <li>
<strong>EIN</strong> and <strong>NAME</strong>—Identification columns</li>
    <li>
<strong>APPLICATION_TYPE</strong>—Alphabet Soup application type</li>
    <li>
<strong>AFFILIATION</strong>—Affiliated sector of industry</li>
    <li>
<strong>CLASSIFICATION</strong>—Government organization classification</li>
    <li>
<strong>USE_CASE</strong>—Use case for funding</li>
    <li>
<strong>ORGANIZATION</strong>—Organization type</li>
    <li>
<strong>STATUS</strong>—Active status</li>
    <li>
<strong>INCOME_AMT</strong>—Income classification</li>
    <li>
<strong>SPECIAL_CONSIDERATIONS</strong>—Special considerations for application</li>
    <li>
<strong>ASK_AMT</strong>—Funding amount requested</li>
    <li>
<strong>IS_SUCCESSFUL</strong>—Was the money used effectively</li>
  </ul>
  <h3>Before You Begin</h3>
  <div class="content-section callout important title-above"><strong class="blockquote-title">important</strong><div>
    <p>The instructions below are now updated to use Google Colab for this assignment instead of Jupyter Notebook. If you have already started this assignment using a Jupyter Notebook then you can continue to use   Jupyter instead of Google Colab.
    </p>
  </div></div>
  <ol>
    <li>
      <p>Create a new repository for this project called <code>deep-learning-challenge</code>. <strong>Do not add this Challenge to an existing repository</strong>.</p>
    </li>
    <li>
      <p>Clone the new repository to your computer.</p>
    </li>
    <li>
      <p>Inside your local git repository, create a directory for the Deep Learning Challenge.</p>
    </li>
    <li>
      <p>Push the above changes to GitHub.</p>
    </li>
  </ol>
 
  <h3>Instructions</h3>
  <h3>Step 1: Preprocess the Data</h3>
  <p>Using your knowledge of Pandas and scikit-learn’s <code>StandardScaler()</code>, you’ll need to preprocess the dataset. This step prepares you for Step 2, where you'll compile, train, and evaluate the neural network model.</p>
  <p>Start by uploading the starter file to Google Colab, then using the information we provided in the Challenge files, follow the instructions to complete the preprocessing steps.</p>
  <ol>
    <li>Read in the <code>charity_data.csv</code> to a Pandas DataFrame, and be sure to identify the following in your dataset:</li>
  </ol>
  <ul>
    <li>What variable(s) are the target(s) for your model?</li>
    <li>What variable(s) are the feature(s) for your model?</li>
  </ul>
  <ol start="2">
    <li>
      <p>Drop the <code>EIN</code> and <code>NAME</code> columns.</p>
    </li>
    <li>
      <p>Determine the number of unique values for each column.</p>
    </li>
    <li>
      <p>For columns that have more than 10 unique values, determine the number of data points for each unique value.</p>
    </li>
    <li>
      <p>Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, <code>Other</code>, and then check if the binning was successful.</p>
    </li>
    <li>
      <p>Use <code>pd.get_dummies()</code> to encode categorical variables.</p>
    </li>
    <li>
      <p>Split the preprocessed data into a features array, <code>X</code>, and a target array, <code>y</code>. Use these arrays and the <code>train_test_split</code> function to split the data into training and testing datasets.</p>
    </li>
    <li>
      <p>Scale the training and testing features datasets by creating a <code>StandardScaler</code> instance, fitting it to the training data, then using the <code>transform</code> function.</p>
    </li>
  </ol>
  <h3>Step 2: Compile, Train, and Evaluate the Model</h3>
  <p>Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.</p>
  <ol>
    <li>
      <p>Continue using the file in Google Colab in which you performed the preprocessing steps from Step 1.</p>
    </li>
    <li>
      <p>Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.</p>
    </li>
    <li>
      <p>Create the first hidden layer and choose an appropriate activation function.</p>
    </li>
    <li>
      <p>If necessary, add a second hidden layer with an appropriate activation function.</p>
    </li>
    <li>
      <p>Create an output layer with an appropriate activation function.</p>
    </li>
    <li>
      <p>Check the structure of the model.</p>
    </li>
    <li>
      <p>Compile and train the model.</p>
    </li>
    <li>
      <p>Create a callback that saves the model's weights every five epochs.</p>
    </li>
    <li>
      <p>Evaluate the model using the test data to determine the loss and accuracy.</p>
    </li>
    <li>
      <p>Save and export your results to an HDF5 file. Name the file <code>AlphabetSoupCharity.h5</code>.</p>
    </li>
  </ol>
  <h3>Step 3: Optimize the Model</h3>
  <p>Using your knowledge of TensorFlow, optimize your model to achieve a target predictive accuracy higher than 75%.</p>
  <p>Use any or all of the following methods to optimize your model:</p>
  <ul>
    <li>Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:
      <ul>
        <li>Dropping more or fewer columns.</li>
        <li>Creating more bins for rare occurrences in columns.</li>
        <li>Increasing or decreasing the number of values for each bin.</li>
        <li>Add more neurons to a hidden layer.</li>
        <li>Add more hidden layers.</li>
        <li>Use different activation functions for the hidden layers.</li>
        <li>Add or reduce the number of epochs to the training regimen.</li>
      </ul>
    </li>
  </ul>
  <p><strong>Note</strong>: If you make at least three attempts at optimizing your model, you will not lose points if your model does not achieve target performance.</p>
  <ol>
    <li>
      <p>Create a new Google Colab file and name it <code>AlphabetSoupCharity_Optimization.ipynb</code>.</p>
    </li>
    <li>
      <p>Import your dependencies and read in the <code>charity_data.csv</code> to a Pandas DataFrame.</p>
    </li>
    <li>
      <p>Preprocess the dataset as you did in Step 1. Be sure to adjust for any modifications that came out of optimizing the model.</p>
    </li>
    <li>
      <p>Design a neural network model, and be sure to adjust for modifications that will optimize the model to achieve higher than 75% accuracy.</p>
    </li>
    <li>
      <p>Save and export your results to an HDF5 file. Name the file <code>AlphabetSoupCharity_Optimization.h5</code>.</p>
    </li>
  </ol>
  <h3>Step 4: Write a Report on the Neural Network Model</h3>
  <p>For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.</p>
  <p>The report should contain the following:</p>
  <ol>
    <li>
      <p><strong>Overview</strong> of the analysis: Explain the purpose of this analysis.</p>
    </li>
    <li>
      <p><strong>Results</strong>: Using bulleted lists and images to support your answers, address the following questions:</p>
    </li>
  </ol>
  <ul>
    <li>
      <p>Data Preprocessing</p>
      <ul>
        <li>What variable(s) are the target(s) for your model?</li>
        <li>What variable(s) are the features for your model?</li>
        <li>What variable(s) should be removed from the input data because they are neither targets nor features?</li>
      </ul>
    </li>
    <li>
      <p>Compiling, Training, and Evaluating the Model</p>
      <ul>
        <li>How many neurons, layers, and activation functions did you select for your neural network model, and why?</li>
        <li>Were you able to achieve the target model performance?</li>
        <li>What steps did you take in your attempts to increase model performance?</li>
      </ul>
    </li>
  </ul>
  <ol start="3">
    <li>
<strong>Summary</strong>: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.</li>
  </ol>
  <h3>Step 5: Copy Files Into Your Repository</h3>
  <p>Now that you're finished with your analysis in Google Colab, you need to get your files into your repository for final submission.</p>
  <ol>
    <li>
      <p>Download your Colab notebooks to your computer.</p>
    </li>
    <li>
      <p>Move them into your Deep Learning Challenge directory in your local repository.</p>
    </li>
    <li>
      <p>Push the added files to GitHub.</p>
    </li>
  </ol>   

</body></html>