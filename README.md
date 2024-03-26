<!DOCTYPE html>
<html lang="en">
<body>
  <h1>Customer Churn Analysis - Readme</h1>
  <section class="section">
    <h2>Understanding Our Data</h2>
   <p>As machine learning engineers,  we must understand the goal of our project in order to get the highest possible accuracy and the most real-world solution to our problem.
“ Churning ” in marketing terms, refers to the number of customers who stopped using a particular product. So, Our project is to predict if the customer will possibly stops using a certain product or not . This will help the company or the market that is selling this product to determine the amount of that product that they will buy.
</p>
    <p>This dataset consists of <i>21</i> columns (Features /Attributes) and <i>7044</i> rows ( Samples/ Cases). 
The types of those features are mixed between numerical and categorical features. This indicated that some of them will be encoded using a Label Encoder.
</p>
  </section>
  <section class="section">
    <h2>Data Visualization</h2>
    <p>It includes:
<ol>
  <li>Plotting the distribution of your data.</li>
  <li>Display the classes of the data for the target column.</li> 
<li>Displaying the correlation matrix to see the relationship between the features.</li>
<li>Getting the statistical analysis of the numerical features in the data suing .describe() method</li>
</ol>
</p>
      </p>
  </section>
  <section class="section">
    <h3>Correlation Matrix</h3>
    <p>A correlation matrix would depict relationships between different data points.
    <img src="https://github.com/SamaHamza/DataAugmentation-CustomerChurn/assets/107436690/7a293b01-8699-492d-a604-54901b28e04c"></p>
  </section>
  <section class="section">
    <h2>Data Preprocessing</h2>
    <p>This section details steps taken to prepare the data for analysis, potentially including:</p>
    <ul>
      <li>Handling missing values: I have used Simple Imputer from Sklearn library.</li>
      <li>Encoding categorical variables: Using Label Encoder.</li>
      <li>Feature scaling: Standardization has been applied. </li>
    </ul>
  </section>
  <section class="section">
    <h2>Model Building & Evaluation</h2>
    <p>Here, different machine learning models were trained and evaluated to predict customer churn:
      <ul>
        <li>AdaBoost Classifier</li>
        <li>Support Vector Machine Classifier</li>
        <li>Gradient Boosting Classifier</li>
        <li>Kernel Approximation</li>
        <li>Logistic Regression</li>
      </ul>
      Evaluation metrics like Training Accuracy, Testing Accuracy, and Validation Accuracy were used for each model.
      <table>
        <thead>
          <tr>
            <th>Model</th>
            <th>Training Acc</th>
            <th>Testing Acc</th>
            <th>Validation Acc</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>AdaBoost Classifier</td>
            <td>80.5%</td>
            <td>80.5%</td>
            <td>79.4%</td>
          </tr>
          <tr>
            <td>Support Vector Machine Classifier</td>
            <td>82.1%</td>
            <td>80.5%</td>
            <td>78.5%</td>
          </tr>
          <tr>
            <td>Gradient Boosting Classifier</td>
            <td>82.8%</td>
            <td>81.5%</td>
            <td>79.7%</td>
          </tr>
          <tr>
            <td>Kernel Approximation</td>
            <td>79.9%</td>
            <td>80.6%</td>
            <td>78.9%</td>
          </tr>
          <tr>
            <td>Logistic Regression</td>
            <td>79.9%</td>
            <td>80.5%</td>
            <td>79.7%</td>
          </tr>
        </tbody>
      </table>
    </p>
  </section>
  <section class="section">
    <h1>Data Augmentation</h1>
    <p>Data augmentation :It’s a technique of artificially increase the training set by creating modified copies of a dataset using existing data. 	It includes making minor changes to the dataset or using deep learning to generate new data points.</p>
    <p>When we should use data augmentation ?
<ul>
  <li>To prevent overfitting.</li>
  <li>Initial training set is too small.</li>
  <li>To improve the model accuracy.</li>
  <li>Reduce the operational coset of labelling and cleaning the raw data.</li>
</ul>
</p>
    <p>What are the limitation of data augmentation ?
    <ol>
      <li>The biases in the original dataset persist in the augmented dataset.</li>
      <li>Quality assurance for the augmented data is expensive.</li>
      <li>Research and development are required to build a system with advanced applications(for deep applications).</li>
      <li>Finding an effective data augmentation approach can be challenging.</li>
    </ol>
    </p>
  </section>
  <section class="section">
    <h2>Results After Data Augmentation</h2>
            Evaluation metrics like Training Accuracy, Testing Accuracy, and Validation Accuracy were used for each model.
      <table>
        <thead>
          <tr>
            <th>Model</th>
            <th>Training Acc</th>
            <th>Testing Acc</th>
            <th>Validation Acc</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>AdaBoost Classifier</td>
            <td>80.5%</td>
            <td>80.1%</td>
            <td>80.1%</td>
          </tr>
          <tr>
            <td>Support Vector Machine Classifier</td>
            <td>75.7%</td>
            <td>75.8%</td>
            <td>75.7%</td>
          </tr>
          <tr>
            <td>Gradient Boosting Classifier</td>
            <td>82.0%</td>
            <td>81.0%</td>
            <td>81.3%</td>
          </tr>
          <tr>
            <td>Kernel Approximation</td>
            <td>76.8%</td>
            <td>76.8%</td>
            <td>76.9%</td>
          </tr>
          <tr>
            <td>Logistic Regression</td>
            <td>79.8%</td>
            <td>79.3%</td>
            <td>79.9%</td>
          </tr>
        </tbody>
      </table>
    </p>
    <hr>
    <table>
        <thead>
          <tr>
            <th colspan="2">Feature Importannce</th>
          </tr>
          <tr>
            <th>With Augmentation</th>
            <th>Without Augmentation</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><img src="https://github.com/SamaHamza/DataAugmentation-CustomerChurn/assets/107436690/520d7d2c-f5dd-41dc-97fe-c7eb13898fdd"></td>
            <td><img src="https://github.com/SamaHamza/DataAugmentation-CustomerChurn/assets/107436690/c77ac2c7-dee7-457d-9cf7-43afad64f870"></td>
          </tr>
        </tbody>
      </table>
    <p> click on this link to see the code:  https://colab.research.google.com/drive/1zCCaL4BZ27SNiBmv2qYJPv3E0BhTDRZ3?usp=sharing</p>

  </section>
</body>
</html>

