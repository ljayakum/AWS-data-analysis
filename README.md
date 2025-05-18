# AWS-data-analysis
## Project Description: Analyzing Netflix Data with Amazon QuickSight
### Overview
In this project, I’m exploring how to use Amazon QuickSight to analyze Netflix data and create visual dashboards. The goal is to gain hands-on experience with cloud-based data visualization tools while uncovering trends and insights from the dataset. This project is part of my journey to learn cloud data services for data analysis.

![over view](https://github.com/user-attachments/assets/adb50724-69b8-4c8c-a39a-2d3558ddfd55)

## 🛠️ Project Steps
### Uploading Data to S3 for QuickSight:

In this step, I’m setting up an S3 bucket on AWS to store the Netflix data files. I will:

1)Create a new S3 bucket

2)Upload the CSV files I want to analyze

3)S3 is used in this project to store two files, which are manifest.json and netflix_titles.csv.

> ✅ **Files stored in S3:**  
> - `manifest.json`  
> - `netflix_titles.csv`

![S3 UPLOAD](https://github.com/user-attachments/assets/8a3bdb9d-a33c-486d-bd86-fe0c9a226d61)

The manifest.json file tells QuickSight about the structure and format of the data we’re analyzing, and netflix_titles.csv is the actual dataset we’re using for analysis in this project.

I edited the manifest.json file by updating the S3 URL to point to our data file, as QuickSight needs this to locate and interpret the dataset correctly.

These files will serve as the data source for my analysis and visualizations in Amazon QuickSight.

### Setting up QuickSight account:

In this step, we will set up an Amazon QuickSight account because we need it to start analyzing our data.
#### Important!!

Creating a QuickSight account costs $0 as it comes with a 30-day free trial—just make sure to uncheck the “Pixel Perfect Report” add-on during sign-up to avoid extra charges.

![quickSight](https://github.com/user-attachments/assets/d88b8813-80a5-4c7e-a574-461bc61166b6)

In this step, we will set up our dataset for visualization by connecting it to QuickSight—QuickSight has permission to access our data, but it won’t load the data until the end of this step.
![setting up work sheet](https://github.com/user-attachments/assets/cbf66921-a00f-47b1-a2f3-a14e19963e83)

I connected the S3 bucket to Amazon QuickSight through the **Datasets** page. Among the available data source options, we selected **S3** to link our dataset for analysis.

The `manifest.json` file was important in this step because it tells QuickSight how to read the data. In this project, it specifies that we're uploading a `.csv` file (spreadsheet) and defines the delimiter (i.e., commas), so QuickSight knows how to parse and break up the data correctly for analysis. Without it, QuickSight might not interpret the file properly.

## 📊 Creating Visualizations in QuickSight

In this step, I will create visualizations using the dataset fields in QuickSight. I will start building lots of different charts to explore patterns, trends, and insights in the Netflix data.

In QuickSight, I simply clicked on data fields like `release_year`, and QuickSight automatically generated a chart that best suited the data type. I also experimented by dragging fields into different sections, like the X-axis and Values area, to customize how the visualizations looked. It was intuitive and helped me quickly build charts to explore the Netflix dataset.
### 📊 Donut Chart: Count of Records by Release Year

![visualization](https://github.com/user-attachments/assets/ac048a97-7e46-4cc5-bc9c-d86144849b7e)

I created a **donut chart** to visualize the distribution of Netflix titles by their release year. The center of the donut shows the total count (8.81K), while the outer segments represent the top 20 release years. This chart helped me quickly identify that most content was added between 2017 and 2020, reflecting Netflix’s recent expansion in content production.

### 🧠 Answering Business Questions

In this step, I answered a few questions that the Netflix team might ask to gain insights from the raw dataset. These questions help uncover trends and patterns in the movies and shows available on the platform. Let’s see what kind of insights we can generate!

### ❓ Business Questions

1) I quite like the breakdown of TV shows/movies for each release year. Would it be possible to stack movies and TV shows in the same row, so you can visualise the % of each?

![q1](https://github.com/user-attachments/assets/0a298fd4-9ab1-4287-b3c5-98afb35f0dd5)

2) Now, can you show me the same thing in a table? I.e., please show me the number of movies vs TV shows of these titles per release year if possible.

![2 table](https://github.com/user-attachments/assets/ddb1155d-29c8-421d-a40b-f3e7c6b49641)

3) On what day did Netflix add the largest number of movies/TV shows to their catalogue?
![3 visual](https://github.com/user-attachments/assets/6227a62c-366e-4942-849c-a63aac7721db)

4) Of the TV shows and movies featured, how many were listed as 'Action & Adventure', 'TV Comedies', or 'Thrillers'? For simplicity, ignore the TV shows and movies that have multiple listings/categories.

![q4](https://github.com/user-attachments/assets/6ee1289e-28da-422c-a2d0-6cf1f2a7cab8)

5) Of the TV shows and movies with the listing 'Action & Adventure', 'TV Comedies', or 'Thrillers', how many were released on 2015 or after?

![q5](https://github.com/user-attachments/assets/580d8660-4cd3-4c4d-8472-55d905aee35c)

### 🔍 Using Filters in QuickSight

Filters are useful for narrowing down the data to a specific subset we want to focus on. In this project, I applied filters to isolate particular genres, release years, or content types (like TV Shows or Movies) 
to answer targeted business questions and gain clearer insights.

### 🔄 Updating the Dataset in QuickSight

If there are any updates or changes made to the dataset (e.g., new records or corrected values), here's how I reflected those updates in QuickSight:

1. Re-upload the updated dataset to the S3 bucket.
2. In QuickSight, go to the **Datasets** tab via the top toolbar.
3. Click on **“Refresh now”** on the left-hand side panel to reload the latest data from the S3 bucket.

This ensures that all visualizations and analyses are based on the most recent version of the dataset.

### ✅ Final Step: Publishing and Sharing the Dashboard

In this **final step**, I added titles to all the charts, published the dashboard, and exported it as a PDF. This allows me to present the visualizations to others and share insights in a professional format. Exporting to PDF is especially useful for sharing with teams or stakeholders who don’t have access to QuickSight.

### 🏷️ Adding Chart Titles Before Publishing

As a final touch before publishing the dashboard, I updated all chart titles to make them more descriptive. The default titles (e.g., just `release_year`) weren’t very informative. So, I renamed them to clearly communicate the chart's purpose — for example:  
**“🎬 Movies vs TV Shows by Release Year”**  
This makes the dashboard more understandable and viewer-friendly.

## What I Learned

Throughout this project, I worked with key AWS services such as **Amazon QuickSight** and **Amazon S3**.  
Some of the important concepts I learned include:

- Working with `manifest.json` files to configure data structure
- Creating and customizing data visualizations (e.g., bar charts, donut charts)
- Applying filters and parameters to refine insights
- Performing cloud-based data analysis using real-world datasets

This project helped strengthen my understanding of cloud data tools and how to build interactive dashboards for meaningful data storytelling.

### 📄 Final Report

You can view the final exported dashboard as a PDF here:  
[Sheet_2_2025-05-18T07_43_05.pdf](https://github.com/user-attachments/files/20271759/Sheet_2_2025-05-18T07_43_05.pdf)







