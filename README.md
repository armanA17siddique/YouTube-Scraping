# YouTube Video Analysis

## Overview

This project analyzes video statistics such as views, likes, and comments from a list of YouTube videos. The data includes video titles, publication dates, and engagement metrics, stored in a CSV file. The project provides insights into video performance over time.

## Features

- Extracts and stores video statistics such as:
  - **Title**
  - **Published Date**
  - **Views**
  - **Likes**
  - **Comments**
  - **Published Month**
- Analyzes YouTube video performance using CSV data.

## Dataset

The dataset used for analysis (`Video_details.csv`) contains the following columns:

- **Title**: Title of the YouTube video.
- **published_date**: Date when the video was published.
- **Views**: Number of views for each video.
- **Likes**: Number of likes each video has received.
- **Comments**: Number of comments on the video.
- **Month**: The month of publication.

### Sample Data

| Title | Published_date | Views | likes | Comments |
|:---|:---|:---|:---|:---|
| The Projects You Should Do To Get A Data Scien... | 2019-07-30 | 158151 | 5761 | 251 |
| What Does a Data Scientist Actually Do? | 2019-07-19 | 70535 | 1454 | 75 |
| Is Data Science Right For You? | 2019-08-18 | 54936 | 1225 | 109 |
| Scrape Twitter Data in Python with Twitterscra... | 2019-04-18 | 47118 | 838 | 315 |
| How To Get Data Science Experience (Without a ... | 2019-08-08 | 30230 | 1387 | 77 |
| Work From Home Data Scientist: Day in the Life | 2019-04-12 | 28623 | 755 | 101 |
| How I Got My First Data Science Internship (An... | 2019-06-21 | 27574 | 1274 | 89 |
| I Wish I Had Known THIS Before Starting in Dat... | 2019-05-14 | 25769 | 1057 | 66 |
| Should You Learn R for Data Science? | 2019-04-25 | 22871 | 576 | 72 |
| Should You Get A Masters in Data Science? | 2018-11-14 | 21426 | 303 | 133 |
## Usage

1. **Prerequisites**:
   - Python 3.x
   - Required Python libraries:
     - `pandas`
     - 'seaborn'

   You can install the required dependencies with:
   ```bash
   pip install pandas
   ```

2. **Running the Analysis**:

   You can load the CSV file and start analyzing the video performance metrics using the following code:

   ```python
   import pandas as pd

   # Load the CSV file
   df = pd.read_csv('Video_details.csv')

   # Display the first few rows of the dataset
   print(df.head())
   ```

   This will provide an overview of the video data and allow further analysis such as identifying the most liked video, most commented, or most viewed.

## Example Analysis

You can use this dataset to perform various analyses, such as:

- **Finding the Most Viewed Video**:

   ```python
   most_viewed = df.loc[df['Views'].idxmax()]
   print("Most Viewed Video:", most_viewed['Title'], "with", most_viewed['Views'], "views.")
   ```

- **Analyzing Video Engagement**:
  Create visualizations of likes, views, and comments to assess which types of videos are performing well.

## Contributing

Feel free to submit issues or pull requests if you have suggestions to improve this project.

## License

This project is licensed under the MIT License.
