# Combining Predictive Techniques

## Dataset

This dataset contains store sales data, store information and store demographic data.

## Summary of Findings

In the exploration, I found that credit grading correlated with interest rates and the loan amounts. Expected relationships were found in the association between the risk estimation and variables considered affecting the risk factor.

It appears that borrowers with lower interest rates have higher credit grades and prospect ratings, bigger loans, are employed and own a home. Most of the current borrowers are employed and have higher credit grades.

The borrowers with higher interest rates, lower prosper ratings, lower monthly income and who are not homeowners end up more often with being late with payments or the loan being defaulted or charged off.

## Key Insights

First, I determined store segments for existing stores by clustering with the K-Means Clustering method which calculated the Adjusted Rand and Calinski-Harabasz indices based on the sales data and more specifically category sales as a percentage of total store sales. The optimal number of store formats according to the highest median was 3.

https://github.com/currentco/data-analytics/blob/main/store_formats/tableau_viz.png



## License

Copyright (c) 2021 Eevamaija Virtanen

This project is licensed under the terms of the MIT license.
