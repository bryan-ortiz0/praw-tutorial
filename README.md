# PRAW Subreddit Scraper Guide 📊

This guide will walk you through the process of using the Python Reddit API Wrapper (PRAW) to scrape data from subreddits using Reddit's API. By the end, you should be able to extract and analyze data from any public subreddit.

## Prerequisites
- Python 3.x installed:
```
pip install python
```
- A Reddit account with developer access--we will work on this on step 2 if needed

## Step 1: Install PRAW
To get started, we need to install the PRAW package. Open your terminal or command prompt and run the following command:
```
pip install praw
```
*Make sure you have administrator privileges before running this command.*

## Step 2: Create a Developer Account
Before we can start scraping data, we need to create a developer account on Reddit and obtain our client ID (`API_KEY`) and our client secret (`API_SECRET`). Just follow these simple instructions:
1. Visit [Reddit](https://www.reddit.com/) and create your account (can be a throwaway account)
2. Navigate to the [Reddit Apps](https://www.reddit.com/prefs/apps) page
3. Click on "are you a developer? create an app..." button on the left
4. When filling out your information to create an application, make sure it looks like this (with your own inputs for name and description):
![reddit praw](https://github.com/bryan-ortiz0/praw-tutorial/assets/130245932/5dbf335e-9524-4237-9d19-1e6c92d5621d)
5. Once your application is submitted, you'll reach a page that looks like the following image and you will copy Client ID & Secret:
![reddit praw2](https://github.com/bryan-ortiz0/praw-tutorial/assets/130245932/339f4ece-6cea-4618-9ebe-2ed23117ce3c)
     - *Remember to keep them confidential*

## Step 3: Authenticate with Reddit
Now that we have our credentials, we'll update the `scraper.py` file that is provided with the necessary information needed to work. Simply replace the placeholders `API_KEY`, `API_SECRET`, `USERNAME`, and `PASSWORD` in `scraper.py` with your own credentials obtained during Step 2.

## Step 4: Gathering Data with a Jupyter Notebook (Credit: Tim Book)
A notebook called `gather_data.ipynb` is provided with code that gathers posts from various sort options in a chosen subreddit and combines the data into a single Pandas DataFrame. Finally, the resulting merged dataset is exported as a CSV file.

The provided code covers the following tasks:
1. Importing the necessary modules--PRAW, the included credentials from `scraper.py`, and Pandas
2. Establishing a Reddit object using your personalized credentials
3. Implementing a utility function `combine_data()` that performs the task of accumulating raw post data extracted from queried sources while tracking temporal metrics linked with each submitted item
4. Designating the target subreddit (''). 👈 **Modify this string as desired.**
5. Acquiring the most recent, popular, high-quality, and disputed posts individually. Each group comprises 1000 entries
6. Consolidating the collected post data by employing the `combine_data()` function
7. Building a comprehensive DataFrame encompassing the consolidated data sets
8. Writing the assembled DataFrame as a CSV file locally (create a folder named 'data' to properly store the csv file)

## Step 5: Explore The Universe Of Subreddits
We now possess all the tools needed to put our skills to work. Try out the code and enjoy the results!

Happy coding! 😊
