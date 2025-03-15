# 90_Day_Fiance_Real_Or_Reality
1. This project aims to explore the dynamics and success rates of relationships featured in TLC's 90 Day Fiancé to shed light on the societal stigma surrounding marriages between US citizens and foreign spouses. By analyzing factors such as age, gender of the US citizens, how couples met, and the shown support from friends and family during the season, my project seeks to provide a data-driven perspective on these relationships. To ground the findings in real-world context, I will also compare the show's trends to broader societal data, including US marriage/divorce rates and K1 fiancé visa applications. This project leverages real societal trends to challenge stereotypes, highlight the complexities of international relationships, and foster a more nuanced understanding of this cultural phenomenon.
2. 90 Day Fiance data compliled by watching and help of ChatGPT. Marriage and Divorce data found through the US Census Bureau (https://data.census.gov/table?q=marriage%20and%20divorce%20in%20kentucky&t=Families%20and%20Living%20Arrangements&g=010XX00US_040XX00US01,04,05,06,09,12,13,16,17,18,20,22,23,24,29,31,32,33,34,35,36,37,39,40,41,42,45,46,47,48,49,51,53,55&y=2023) and K1 Non-Immigrant Petition Data by the US State Department (https://travel.state.gov/content/travel/en/legal/visa-law0/visa-statistics/nonimmigrant-visa-statistics/monthly-nonimmigrant-visa-issuances.html)
3. Identify and describe three or more features you integrated from the provided list.
    
    A. Percent of 90 Day couples that did get married, and percent of couples that are still together
    
    B. Does how couples meet influence if they are still togehter?
    
    C. Does having support of friends and family influence if they are still together?
    
    D. Percent of US spouse being male or female influence?
   
    E. Does age influence if they are still together?
    
    F. Compare counties represented in the series to issuances of K1 petitions
    
    G. Compare percent by US state of couples in the series to the corresponding state marriage / divorce

4. Include any special instructions for reviewers to run your project.

    A. Either be a lover or a hater for reality shows and the complexities of marriage and immigration. 

    B. Tools and Technologies: Jupyter Notebook with Pandas, Plotly, Matplotlib, NumPy, Seaborn. When using a virtual environment, you'll need to install these tools prior to use. 

    C. There is a plotly map avaiable to interact with it, please fork this repo and run in a Jupyter Notebook. 

    D. Creating and Using Virtual Environments:

**Create a Virtual Environment:** Virtual environment are one of the things   
that you need to do in the terminal. Its a vital skill that is expected in    
the industry. 

## Virtual Environment Commands

| Command | Linux/Mac | GitBash |
| ------- | --------- | ------- |
| Create | `python3 -m venv venv` | `python -m venv venv` |
| Activate | `source venv/bin/activate` | `source venv/Scripts/activate` |
| Install | `pip install -r requirements.txt` <br> or pip install packages | `pip install -r requirements.txt` <br> or pip install packages |
| Deactivate | `deactivate` | `deactivate` |

**In your project folder** 
- run python -m venv myenv (where myenv is the name of your virtual environment typically venv).

**Activate the Environment:**

- On Windows, use myenv/Scripts/activate.
- On macOS/Linux, use source myenv/bin/activate

**Install Packages:**

- Use pip install <package_name> to install packages that are needed for your project.

**Deactivate the Environment:**

- When you're done working, type deactivate to return to your global environment.

---



5. Data set dictionaries


## A. 90 Day Fiancé Dataset
This dataset contains information on couples featured in seasons 1-10 of *90 Day Fiancé*.

| Column Name       | Data Type  | Description |
|------------------|-----------|-------------|
| Couple_ID       | Integer   | Unique identifier for each couple in *90 Day Fiancé* |
| Season         | Integer   | The season in which the couple appeared |
| US_State       | String    | The US state where the American partner resides |
| Wed           | Boolean   | Whether the couple got married (1 = Yes, 0 = No) |
| Still_Together | Boolean   | Whether the couple is still together (1 = Yes, 0 = No) |
| Age_Gap       | Integer   | The age difference between partners in years |
| How_They_Met  | String    | How the couple met (e.g., "Online," "Vacation," "Mutual Friends") |
| K1_Visa_Approved | Boolean | Whether the couple received K1 visa approval (1 = Yes, 0 = No) |

---

## B. US Census Bureau Dataset
This dataset provides national and state-level marriage and divorce statistics.

| Column Name         | Data Type  | Description |
|--------------------|-----------|-------------|
| Year             | Integer   | Year of the reported data |
| US_Marriage_Rate | Float     | US marriage rate per 1,000 population |
| US_Divorce_Rate  | Float     | US divorce rate per 1,000 population |
| Total_Population | Integer   | Total US population in the given year |
| Married         | Integer   | Number of currently married individuals |
| Divorced       | Integer   | Number of divorced individuals |
| Separated      | Integer   | Number of legally separated individuals |
| Widowed        | Integer   | Number of widowed individuals |

---

## C. US State Department Dataset
This dataset contains data on K1 visa applications and approvals.

| Column Name   | Data Type | Description |
|--------------|----------|-------------|
| Nationality  | String   | Country of Applicant |
| Visa Class   | String   | Type of Visa, we are interested in K1 for this project |
| Issuances    | Integer  | Total number of visas approved |



    D. Data Transformations
Wed and Still_Together values were converted to binary (1 = Yes, 0 = No).
US_State was standardized for consistency across datasets.
Marriage and divorce rates were normalized per 1,000 people for better comparability.
Merged datasets using Year and US_State to align census and visa statistics with 90 Day Fiancé data.

6. Next steps: continue to expand the data through repeating patterns by uear of US Census, and combining months and years from the State Department for total K1 petitions. Build into a dashboard and/or Tableau.