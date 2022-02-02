# Ubiquant-Market-Prediction
Ubiquant Investment (Beijing) Co., Ltd is a leading domestic quantitative hedge fund based in China. Established in 2012, they rely on international talents in math and computer science along with cutting-edge technology to drive quantitative financial market investment. Overall, Ubiquant is committed to creating long-term stable returns for investors.



## Data Description
This dataset contains features derived from real historic data from thousands of investments. Your challenge is to predict the value of an obfuscated metric relevant for making trading decisions.

This is a code competition that relies on a time-series API to ensure models do not peek forward in time. To use the API, follow the instructions on the Evaluation page. When you submit your notebook, it will be rerun on an unseen test. This is also a forecasting competition, where the final private leaderboard will be determined using data gathered after the training period closes, which means that the public and private leaderboards will have zero overlap.

## File
train.csv

row_id - A unique identifier for the row.
time_id - The ID code for the time the data was gathered. The time IDs are in order, but the real time between the time IDs is not constant and will likely be shorter for the final private test set than in the training set.
investment_id - The ID code for an investment. Not all investment have data in all time IDs.
target - The target.
[f_0:f_299] - Anonymized features generated from market data.
example_test.csv - Random data provided to demonstrate what shape and format of data the API will deliver to your notebook when you submit.

example_sample_submission.csv - An example submission file provided so the publicly accessible copy of the API provides the correct data shape and format.

ubiquant/ - The image delivery API that will serve the test set. You may need Python 3.7 and a Linux environment to run the example test set through the API offline without errors.

Time-series API Details - The API serves the data in batches, with all of rows for a single time time_id per batch.

-Expect to see roughly one million rows in the test set.

-The API will require roughly 0.25 GB of memory after initialization. The initialization step (env.iter_test()) will require meaningfully more memory than that;     we recommend you do not load your model until after making that call.

-The API will also use less than 15 minutes of runtime for loading and serving the data.

