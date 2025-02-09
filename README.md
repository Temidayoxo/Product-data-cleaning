# Marketing Data Optimization:
Cleaning,Standardization, and SEO-Driven Title
Enhancement
# OVERVIEW
The dataset, productdata.xlsx , contains product-related information, including product IDs, titles, bullet points, descriptions,
product types, and dimensions. This dataset was provided in Excel format and served as the primary source for the data
cleaning process. It was provided by HNG Tech as part of the internship program, serving as a practical case study for
applying data cleaning, standardization, and optimization techniques.
Using the data.shape function, it was discovered that the dataset contains 3,847 rows and 6 columns, providing a
comprehensive set of product data for analysis.
[Download dataset here](https://docs.google.com/spreadsheets/d/18p4cUhyvUpRzpaq2fzCj1EmKcZyk9PmG/edit?usp=drive_link&ouid=103126208255939870793&rtpof=true&sd=true).
# This report outlines the steps taken to clean and process the dataset.

The data cleaning process focused on identifying and addressing missing values, removing duplicates, standardizing formats, and creating short product titles to improve readability.

1. Duplicate Removal:
 Duplicates were identified and removed based on the PRODUCT_ID column, reducing the dataset from 3,847 rows to 3,630 rows.This ensured that the entry in the dataset was unique.

2. Handling Missing Values:

 The BULLET_POINTS and DESCRIPTION columns had many empty entries. These were filled with "Not specified" to indicate missing details.

Additional cleaning steps were taken to further improve data quality:

Product_type_id: Missing values were replaced with mode ,which is the most frequent occurring value in the column. This decision as made because product_type_ids are categorical, and using the most common category maintained data consistency. The mode was calculated using  Excel’s formula : =MODE(E2:E3631). The result was used to replace all the missing values.
Product_length: Missing values were replaced with median to avoid the influence of extreme values.The median was calculated using Excel’s formula : =MEDIAN(F2:F3631). This ensured that the product _lengths column data were maintained without skewing the data.

3. Standardizing Column Names:
The column names had inconsistent capitalizations and were converted to lowercase with underscores to maintain a consistent format.

4. Data type consistency:
 I ensured all numeric columns were properly formatted as numbers and text column as text.


  Short Title Creation 

Product titles were too long, making them hard to read. To make them shorter and simpler while retaining the key information,Short titles were created by extracting the first meaningful part of the original titles and  limiting them to 50 characters.This step improved readability of the dataset, especially for analysis and purpose. 

Excel formula used :
The following formula was applied to automatically generate short titles: =LEFT(B2,50)
(B2 represents the cell containing the product title). This formula keeps only the first 50 characters of each title, ensuring concise yet informative entries.Then i used Excel’s formula “=Text.Select([Columnname], {"A".."Z", "a".."z", " "})” to remove all special characters and keep all the letters within the range.
 
Examples:
• "ArtzFolio Tulip Flowers Blackout Curtain for Door & Window" 
As
 "ArtzFolio Tulip Flowers Blackout Curtain for Door"

• "ALISHAH Women's Cotton Ankle Length Leggings Combo of 2, Plus 12 Colors_L"  
As 
"Alishah Women's Cotton Ankle Length Leggings Combo”



Clean Dataset Overview

After cleaning, the dataset now has:

No missing or negative values

3,630 unique product entries

Column headers were standardised to lowercase with underscores

Complete and consistent data in all columns

Short and readable product titles

Clear placeholders for missing data


This clean version is saved as ’cleaned _product_data’ which is better organized and ready for further use in analysis or reporting tasks.
# Here's the link to the cleaned dataset 
(https://docs.google.com/spreadsheets/d/1PtQ2xA81Kyf_R_tSbKRtrQJlo3HnmJ4O/edit?usp=drive_link&ouid=103126208255939870793&rtpof=true&sd=true).
