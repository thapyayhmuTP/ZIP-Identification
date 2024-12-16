# ZIP-Identification
A simple project

**Objective:**
I assisted my friend with a school project aimed at identifying ZIP codes with the highest and lowest volatility in prices over the past five years. The project also explored the key drivers of volatility for the year 2022, with a focus on how prices varied over time.

**Data:**
The analysis utilized data from the Zillow Observed Rent Index (ZORI) and Zillow Home Value Index (ZHVI), both based on ZIP codes (similar to postal codes in Canada). Additionally, economic and demographic data for 2022 from Altus Group were incorporated. The original file "zhvi_sm_sa_mont.csv" file was too big to upload so I reduced and splitted into 6 parts. And the summary of the process is explained below.

Explanation of the Reduction and Optimization Process:
1. Original File
The original file was large due to:
  - Many rows and columns (ZIP codes, monthly data, etc.).
  - High numerical precision (long decimals in numerical data).
  - Redundant or less-relevant metadata (e.g., columns not essential to the project).

2. Optimization Steps
To reduce the file size, I followed these steps:
a. Dropped Irrelevant Columns
    - Kept only the columns necessary for the analysis:RegionID (ZIP code), RegionName, StateName, and all columns with price data (e.g., monthly price trends).
    - Removed columns like Metro, CountyName, etc., which were not directly relevant to the objective.
b. Reduced Numerical Precision
    - Rounded all numerical values (e.g., monthly price data) to two decimal places instead of keeping long floating-point numbers (e.g., 1234.56789 → 1234.57).
    - This significantly reduced the file size without losing meaningful data for the analysis.
c. Saved in Optimized Format
    - Saved the optimized dataset in .csv format and compressed it further into .gz to shrink the file size while retaining compatibility.
    - 
3. Splitting into Smaller Parts
After optimization, the file was still slightly over GitHub’s 25MB limit.
To resolve this, I:
  - Calculated Row Size: Split the file into chunks of 5000 rows each.
  - Saved in Separate Files: Ensured every part stayed below the 25MB limit by checking their sizes after splitting.

**Note:** This project was a bit challenging and still **imperfect and imcomplete**, but it was an exciting and rewarding experience to support my friend and work through the complexities together. I’m writing this down as a cherished memory! 😊
