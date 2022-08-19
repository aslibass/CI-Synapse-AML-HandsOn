# CI-Synapse-AML-HandsOn
A Hands On Tutorial on using Dynamics 365 Customer Insights, Azure Synapse and Azure Machine Learning together

| <img src="media/image1.png" style="width:0.80645in;height:0.80645in" alt="A picture containing drawing Description automatically generated" /> |
|------------------------------------------------------------------------------------------------------------------------------------------------------|

<table>
<colgroup>
<col style="width: 90%" />
<col style="width: 9%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Hands-On Lab</p>
<p>Customer Insights, Synapse and Azure Machine Learning</p></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Agenda</td>
<td></td>
</tr>
<tr class="even">
<td><strong>Introduction</strong></td>
<td><strong>30 mins</strong></td>
</tr>
<tr class="odd">
<td><p><strong>Dynamics 365 Customer Insights</strong></p>
<ul>
<li><p>Using CI to Cleanse &amp; Enrich a set of Customer Records </p></li>
</ul></td>
<td><strong>4 hours</strong></td>
</tr>
<tr class="even">
<td><p><strong>Azure Synapse</strong></p>
<ul>
<li><p>Using Synapse to wrangle a set of files </p></li>
</ul></td>
<td><strong>8 hours</strong></td>
</tr>
<tr class="odd">
<td><p><strong>Azure Machine Learning</strong></p>
<ul>
<li><p>Using Azure Machine Learning to find the best predictive model for our business scenario. </p></li>
</ul></td>
<td><strong>2 hours</strong></td>
</tr>
<tr class="even">
<td><strong>Putting it all together</strong></td>
<td><strong>2 hours</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Using CI to navigate, segment, and predict behavior across our final customer dataset.</p></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

Introduction

Add blurb here


Dynamics 365 Customer Insights

Add Dynamics Content here


AZURE SYNAPSE

Now that you’ve exported the profiled customers from Customer Insights,
lets create a larger dataset that we can use to predict if a customer
will renew their lease agreement, and for how long.

In order to predict this we need to add as much information as possible.
Here we will combine the datasets describing

-   Customers (you used CI in the previous step to create this cleaned
    and enriched set.)

-   Leases

-   Properties

-   Workorders

-   Surveys

In your synapse studio, we will examine each file individually, decide
what elements we want to keep and combine. You can load any file to the
spark cluster, by right clicking it and selecting “load to data frame”.
This will create a PySpark notebook for you. Attach this notebook to the
cluster and run the notebook. You should see a table generated in the
cell below. The display() command creates these results which can be
changed to a chart as well. Once you’ve seen what the dataset has, lets
load the others in and combine them into a table that we want. Some
tables require additional steps like pivoting , grouping, renaming, and
conditionally changing values or adding new calculations. To help you
with this, an example notebook has been created with all the steps in
it, but you may need to adjust to your selected datasets/columns as
required. A cheat sheet has also been created with helpful hints. Where
possible we use the simplest approaches which are also scalable.

-   Notebook that combines all the datasets

-   Cheatsheet

Please work your way through the notebook, referring to the cheatsheet
if necessary. Once you have created your final tables, you can continue
to the next step of building a Machine Learning Model that can be
consumed by Customer Insights.

Azure MAchine LEarning

Add AML content here 

<img src="media/image2.jpeg" style="width:3.71042in;height:2.60347in" /><img src="media/image3.jpeg" style="width:3.66944in;height:2.32222in" /><img src="media/image4.jpeg" style="width:2.71042in;height:7.66944in" /><img src="media/image5.jpeg" style="width:3.68611in;height:1.32222in" /><img src="media/image6.jpeg" style="width:3.62778in;height:3.62778in" /><img src="media/image7.jpeg" style="width:3.62778in;height:7.67778in" /><img src="media/image8.jpeg" style="width:4.07431in;height:4.30556in" /><img src="media/image9.jpeg" style="width:7.49583in;height:4.47917in" /><img src="media/image10.jpeg" style="width:7.4875in;height:4.025in" />

