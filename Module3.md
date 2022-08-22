Nw# Module 3

## Azure Machine Learning

### Using Azure Machine Learning to find the best predictive model for our business scenario

Now that we have created our training and testing datasets, lets use Azure Machine Learning from within Synapse to figure out the best model for our purposes. 

In our case, we want to predict
1. Will a Customer Renew their Lease?
2. If so, for how long for?

In addition we also want to understand the most important drivers behind lease renewals, so that we can focus management on these aspects and hopefully improve the future performance of the firm.

### Training a Model from Synapse
Since we've added a Linked Service pointing to Azure Machine Learning, we're able to use the Automated Machine Learning feature directly from Synapse

Navigate to your training data table in the Lake Database. Right Click and select "Train a New Model" under the Machine Learning menu.

![Train Model From Lake Table](./media3/trainmodelfromtable.jpg)

On the next screen we're given the choice of three kinds of problems that can be solved using Automated Machine Learning. Since we want to predict the average renewal length, we will pick Regression.

![Regression AutoML](./media3/selectRegression.jpg)

We then want to select the target column and the available spark cluster.

![Target Column](./media3/targetcolumn.jpg)

Finally, we want to **(Important!)** set the Maximum Training Job Time to 1 (hour) and **(Also Important!)** Enable the ONNX model compatibility so that the DW (and other tools) can work with our model. We then want to **(Important Again!)** Open in Notebook. 

[Enable ONNX](./media3/onnxmodel.jpg)

This generates a notebook with PySpark code to setup an automated machine learning experiment. If needed you can tweak AutoML settings here. Run the notebook. You should get a link to the job, which you can monitor from within Azure Machine Learning Studio. 


### Understanding the outputs of the Model
Login to the Azure Machine Learning Studio, and look for the Experiment that your notebook submitted. After about an hour you should see a completed experiment. 

### Testing a Model from Synapse

