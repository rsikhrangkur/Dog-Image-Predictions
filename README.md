# Dog Image Predictions
### by Ryan Sikhrangkur

## Project Summary
This project is an analysis into the Twitter account WeRateDogs® (@dog_rates), and was submitted for the completion of Udacity's data analysis nanodegree program. The project is divided into three primary Jupyter Notebooks.

### wrangle_act
The wrangle_act.ipynb file contains the entirety of my data analysis work required for the following two notebooks, which would reference the work performed here to present one internal report and one external report.
### wrangle_report
The wrangle_report.ipynb file acts as an internal report (e.g. a department memo) of my investigation of the @dog_rates account. The investigation was conducted in three major steps of gathering data, assessing data, cleaning data, and repeat. Once complete the data was then saved to a master file for potential future analyses.
### act_report
The act_report.ipynb file acts as an external report (such as a blog or magazine highlight), which was written to highlight observations and visualizations made after exploring the master file created for the wrangle_report portion of the project.

## Analysis Details
Gathering of the data was performed through three separate methods:
> Reading the provided twitter_archive_enhanced.csv file into the df_archive dataset.
> Web/data scraping the provided URL and storing the results into the image_predictions.tsv file, and then reading the file into the df_predictions dataset.
> Using the Twitter API Tweepy to query additional data from the @dog_rates account and saving it to the tweet-json.txt file*, and then reading the file into the df_likes_rts dataset.

Assessing the data helped identify any issues present in the three files, with guidance from two conditions: the tweets must be original (no retweets), and exclude tweets made beyond the date of August 1, 2017.
The issues found were defined and divided by whether it was an issue with quality or tidiness, and further separated by dataset where the issue was present.
In total, there were nine quality issues and three tidiness issues.

Cleaning the data was performed in priority of missing data → tidiness issues → quality issues. Upon completion I merged the separate datasets into one, and saved it to the twitter_archive_master.csv file to be used in the act report.

## Analyzing and Visualizing Data
For the act report I analyzed the df_master data to report findings in the format of an interesting yet short internet blog post to highlight the content found in the @dog_rates twitter account, addressing three facts with one subpoint each.

Additionally I had written a code which read through all text of every tweet in the dataset, and using the dog-silhouette-1.png as a mask created a wordcloud shaped like a dog using the most prominent words.