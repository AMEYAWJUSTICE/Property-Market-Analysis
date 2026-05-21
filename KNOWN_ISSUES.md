

# **Known Issues — Project 9 · Team 1**

*NYC Property Market Analysis*

This section documents data quality challenges, analytical decisions, and observations encountered during the project.

---

## **1. Data Quality Issues**

* **Large Data Reduction:**
  The dataset was reduced from **84,548 raw records to 24,668 cleaned records**, which may lead to potential data loss and bias.

* **Missing and Incomplete Values:**
  Some records contained missing values in key fields such as sale price, square footage, and building classification, requiring removal or filtering.

* **Outliers in Sale Price:**
  Extremely high-value transactions (luxury properties) created significant skewness (**16.17**), affecting average calculations.

* **Inconsistent Property Categories:**
  Only Categories 01–03 (residential) were retained to ensure consistency, excluding mixed-use or commercial properties.

* **Data Duplication and Noise:**
  Certain entries showed inconsistencies or possible duplicates, which were cleaned during preprocessing.

---

## **2. Query Cost Notes**

* **Efficient Data Filtering:**
  Early filtering of relevant categories significantly reduced query execution time and improved performance.

* **Aggregation Optimisation:**
  Grouping by borough and neighbourhood was optimised using indexed columns to reduce computation cost.

* **Avoidance of Redundant Queries:**
  Repeated calculations (e.g., average price) were converted into reusable measures in Power BI to minimise processing overhead.

* **Dataset Size Management:**
  Working with a reduced dataset improved dashboard responsiveness and visualisation speed.

---

## **3. Analytical Decisions**

* **Use of Median Alongside Mean:**
  Due to high skewness, the **median price ($590K)** was used alongside the mean ($757K) to provide a more accurate market representation.

* **Focus on Residential Properties Only:**
  To maintain consistency, only residential building classes were included in the analysis.

* **Luxury Property Definition:**
  Properties priced at **more than 2× the average price** were classified as luxury (1,166 properties identified).

* **Time Frame Selection:**
  Analysis was limited to **September 2016 – August 2017** to ensure a consistent yearly comparison.

* **Borough-Level Aggregation:**
  Boroughs were used as primary segmentation for high-level insights, with neighbourhoods for deeper analysis.

---

## **4. Open Questions**

* What external factors (e.g., interest rates, policy changes) influenced the observed price growth?
* How would the inclusion of multiple years affect trend accuracy and forecasting?
* What is the impact of rental market dynamics on property sales?
* Are there emerging neighbourhoods outside Manhattan with future growth potential?
* How do economic indicators correlate with real estate price fluctuations?

---

## **Summary**

Despite data limitations, the project successfully delivered meaningful insights into the NYC property market. The analytical decisions made ensured data consistency, reliability, and relevance for real-world applications.

