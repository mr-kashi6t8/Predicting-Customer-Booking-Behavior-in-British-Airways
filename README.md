<!-- README.md (HTML format) -->

<h1>📌 Project Name</h1>
<h2>"Predicting Flight Booking Completion using Machine Learning"</h2>

<h2>📖 Project Description</h2>
<p>
  This project focuses on predicting whether a customer will complete a flight booking based on their booking behavior, demographics, and travel preferences.
  Using a dataset of customer flight bookings, the project explores the data through <b>EDA (Exploratory Data Analysis)</b>, performs data cleaning and feature engineering,
  and builds a machine learning pipeline for classification.
</p>

<hr />

<h2>🔹 Key Steps in the Project</h2>

<h3>Data Understanding &amp; Cleaning</h3>
<ul>
  <li>Inspected dataset with <code>.info()</code>, <code>.describe()</code>, and <code>.head()</code></li>
  <li>Removed outliers using <b>IQR</b> method</li>
  <li>Handled missing values where necessary</li>
  <li>Created <code>booking_urgency = purchase_lead / (flight_day + 1)</code></li>
</ul>

<h3>Exploratory Data Analysis (EDA)</h3>
<ul>
  <li>Visualized distributions &amp; correlations</li>
  <li>Checked class balance of target (<code>booking_complete</code>)</li>
</ul>

<h3>Feature Engineering &amp; Preprocessing</h3>
<ul>
  <li>One-Hot Encoding for low-cardinality categorical features (<code>sales_channel</code>, <code>trip_type</code>)</li>
  <li>Target Encoding for high-cardinality features (<code>route</code>, <code>booking_origin</code>)</li>
  <li>Standardized numerical features (e.g., <code>booking_urgency</code>)</li>
</ul>

<h3>Model Building</h3>
<ul>
  <li>Built a <b>Pipeline</b> with preprocessing + <b>Random Forest Classifier</b></li>
  <li>Handled imbalance with <code>class_weight="balanced"</code></li>
  <li>Data split: <b>80% Train / 20% Test</b></li>
</ul>

<hr />

<h2>🔹 Model Evaluation</h2>
<ul>
  <li><b>Accuracy:</b> 0.855 (85.5%)</li>
  <li><b>Precision:</b> 0.87 (Class 0), 0.51 (Class 1)</li>
  <li><b>Recall (Sensitivity):</b> 0.98 (Class 0), 0.13 (Class 1)</li>
  <li><b>F1-Score:</b> 0.92 (Class 0), 0.20 (Class 1)</li>
  <li><b>ROC-AUC Score:</b> 0.785</li>
  <li><b>Confusion Matrix:</b> [[6743, 143], [1026, 150]]</li>
</ul>


<hr />

<h2>🔹 Key Insights</h2>
<ul>
  <li>Most important features influencing booking completion:</li>
  <ul>
    <li><b>Route</b> (origin-destination pair)</li>
    <li><b>Booking Origin</b> (country of booking)</li>
    <li><b>Booking Urgency</b> (time gap between booking &amp; flight day)</li>
    <li><b>Flight Duration</b></li>
    <li>Customer add-ons: <b>extra baggage</b>, <b>preferred seat</b>, <b>in-flight meals</b></li>
  </ul>
  <li>Customers with shorter booking urgency (last-minute bookings) are less likely to complete.</li>
  <li>Add-ons (meals, baggage, seat preference) increase booking completion probability.</li>
</ul>

<hr />

<h2>🎯 Final Outcome</h2>
<p>
  The project demonstrates how machine learning can be used to predict booking completion with <b>85% accuracy</b> and <b>0.785 ROC-AUC</b>,
  enabling airlines and travel companies to:
</p>
<ul>
  <li>Identify customers at risk of drop-off</li>
  <li>Personalize offers to improve conversions</li>
  <li>Optimize marketing strategies for higher revenue</li>
</ul>

<p align="center"><i>Made with Python &amp; Scikit-learn • Contributions welcome</i></p>
