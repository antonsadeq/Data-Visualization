# Data-Visualization
Data analysis project focused on analyzing a given dataset and visualizing insights to extract meaningful information.

# Dataset Description:
The dataset used in this project is the **Human Development Report** dataset, containing all composite indices over its complete time series. It was obtained from the **United Nations Development Programme (UNDP)** and can be accessed at: [HDR Dataset](https://hdr.undp.org/sites/default/files/2023-24_HDR/HDR23-24_Composite_indices_complete_time_series.csv).  

This dataset provides valuable insights into **global development trends**, examining nations from both **sociological and economic perspectives**. The attributes primarily consist of **composite indices**, such as the **Human Development Index (HDI), Gender Inequality Index (GII), and Multidimensional Poverty Index (MPI)**, alongside a few **one-dimensional attributes** that reflect development changes over time. Covering multiple decades, this dataset enables a historical analysis of how various factors—such as economic growth, policy changes, or global events—have shaped national development.  

We selected this dataset because of its wide variety of indicators, which allow for in-depth exploration of diverse topics such as economic growth, education levels, healthcare accessibility, and social inequality. The dataset's comprehensiveness makes it ideal for generating meaningful hypotheses across multiple disciplines, including economics, sociology, and public policy.  

Although the dataset is extensive, it is well-structured, with attributes thoughtfully selected to ensure clarity and usability. Its scope and depth make it an excellent resource for understanding global development trends and policy effectiveness over time.  

## Hypotheses & Research Questions

- **Comparison of Economic Recovery**  
  - Investigating whether the **labor force participation rate (LFPR)** and **gross domestic product (GDP)** recovered more quickly in the **USA** compared to **South Korea** following economic crises.  

- **Correlation Between HDI and GII in Asia**  
  - Examining whether an increase in the **Human Development Index (HDI)** is directly proportional to the rise of the **Gender Inequality Index (GII)** in **Asian countries**.  

- **Impact of Education on Income Growth**  
  - Analyzing the effect of an increase in **mean years of schooling (MYS)** on **gross national income per capita (GNIPC)** after **15 years**, using regression analysis to determine deviations from the expected 
    growth trend.

# 📊 Analyizing **labor force participation rate (LFPR)** and **gross domestic product (GDP)** in the **USA** compared to **South Korea** following economic crises

### 🔹 **Data Preprocessing**  
- **Loaded the dataset** and filtered data for only **USA** and **South Korea**.  
- **Selected key attributes:**  
  - **LFPR (Labor Force Participation Rate)**  
  - **GNIPC (Gross National Income per Capita)** (used as a proxy for GDP).  
- **Handled missing values** and ensured data consistency.  
- **Formatted the dataset** for visualization.

---

### 🔹 **Visualization Using Plotly Express**  
- Created a **multi-line chart** to compare **LFPR and GNIPC trends** over time for both countries.  
- Mapped:  
  - **LFPR** on the **left y-axis** (blue).  
  - **GNIPC** on the **right y-axis** (red).  
- **Added vertical reference lines** to highlight key economic crises:  
  - **1997 Asian Financial Crisis** (green dashed line).  
  - **2008 Global Financial Crisis** (orange dashed line).  
- Styled the visualization with **distinct colors, legends, and labels** for clarity.


# 📊 Analyzing the Relationship Between HDI and GII in Asian Countries  

## 🔹 **Objective**  
This analysis explores whether an **increase in Human Development Index (HDI) is directly proportional to a rise in the Gender Inequality Index (GII)** across **Asian countries**. The goal is to understand how human development influences gender inequality trends.  

---

## 🔹 **Data Preprocessing & Challenges**  
- **Loaded the dataset** containing **HDI, GII, and country-level data** for multiple years.  
- **Filtered the dataset** to focus exclusively on **Asian countries** to ensure a region-specific analysis.  
- **Aggregated HDI and GII values** by computing their **sum per country**, allowing a clearer comparison between nations.  
- **Addressed dataset biases**: Some countries were incorrectly assigned to the wrong regions, which required **manual correction** in Power BI’s **Power Query Editor**.  

---

## 🔹 **Visualization Approach in Power BI**  

### **1️⃣ Key Influencers Visualization**  
The **Key Influencers** visual in Power BI was used to determine the **main factors impacting GII** across Asian countries. This analysis helps identify **whether HDI is a primary driver of gender inequality** or if other hidden variables influence the trends.  

### **2️⃣ Scatter Plot for Correlation Analysis**  
A **scatter plot** was created to visually analyze the correlation between:  
- **X-axis:** **Sum of HDI per country**  
- **Y-axis:** **Sum of GII per country**  
- **Color Encoding:** Each country is color-coded to distinguish trends across nations.  

This **scatter plot** provides a **visual representation of the relationship** between HDI and GII, allowing us to see whether **higher HDI values correspond to increased or decreased gender inequality**.

---

## 🔹 **Implementation Steps in Power BI**  

### **Step 1: Data Transformation (Power Query Editor)**  
- Filtered the dataset to **retain only Asian countries**.  
- Corrected **misclassified country regions** (e.g., ensuring Japan, India, and China were correctly assigned).  
- Created **aggregated measures** to compute the **sum of HDI and GII for each country**.  

### **Step 2: Key Influencers Analysis**  
- Used the **Key Influencers visual** in Power BI to determine whether **HDI has a statistically significant impact on GII**.  
- The model **ranked HDI against other potential influencing factors**, providing insights into its impact on gender inequality.  

### **Step 3: Scatter Plot Visualization**  
- Created a **scatter plot** to compare the **sum of HDI vs. sum of GII** per country.  
- Added **color coding** to distinguish **different countries**.  
- Included **interactive filtering options** to allow users to explore specific nations or regions.  

---

## 🔹 **Key Insights & Findings**  
- **Inverse Correlation Observed**: In most cases, **higher HDI correlates with lower GII**, suggesting that human development contributes to **reducing gender inequality**.  
- **Regional Differences**:  
  - **East Asian countries (e.g., Japan, South Korea)** show **rapid HDI growth and decreasing GII**.  
  - **South Asian countries (e.g., India, Pakistan)** have **slower HDI growth and relatively high GII**.  
- **Key Influencers Analysis Findings**:  
  - **HDI was identified as a significant factor influencing GII**, but additional economic and social factors also contribute.  
  - Some countries show **anomalous behavior** where GII remains high despite increasing HDI, highlighting **possible cultural or policy-related barriers**.  

---

## 🔹 **Future Enhancements & Next Steps**  
✅ Use **Power BI’s Decomposition Tree** to further analyze hidden relationships between **HDI, GII, and other economic indicators**.  
✅ Introduce **trend lines** in the scatter plot to reinforce the correlation patterns.  
✅ Experiment with **different aggregation methods** (e.g., mean vs. sum) to see if results remain consistent.  

🚀 **This Power BI visualization effectively demonstrates the relationship between HDI and GII across Asian countries, helping us understand the broader impacts of human development on gender inequality.**  


---
## 🎓📈 Impact of Education on Economic Growth Over Time  

### 🔹 **Objective**  
This analysis explores the relationship between **Mean Years of Schooling (MYS)** and **Gross National Income per Capita (GNIPC)** over time, assessing whether an increase in education levels leads to significant changes in economic growth after **15 years**. The study leverages **regression analysis** to determine deviations from the expected growth trend.

---
### 🔹 **Data Preprocessing & Challenges**  
- **Loaded the dataset** containing **education (MYS) and income (GNIPC) data** for multiple countries over several decades.  
- **Filtered data** to focus on **relevant attributes**:
  - **Mean Years of Schooling (MYS)** – Average years of schooling per individual.  
  - **Gross National Income per Capita (GNIPC)** – A measure of a country's economic output per person.  
- **Classifying countries by region posed a challenge**, as the dataset contained misclassified regions. For example, **Japan was incorrectly categorized as an African country**.  
- **Cleaned and corrected the dataset** by mapping countries to their correct regions, ensuring accuracy in regional comparisons.  
- **Formatted the data** for visualization and analysis.  

---

### 🔹 **Visualization Using Plotly Express**  
To visualize the relationship over time, we created an **animated scatter plot** using **Plotly Express**.  
- **X-axis:** Mean Years of Schooling (MYS).  
- **Y-axis:** Gross National Income per Capita (GNIPC).  
- **Color Encoding:** Each country's region, helping to identify patterns across different global areas.  
- **Time Animation:** A **year slider** was added to illustrate changes dynamically from **1990 to 2020**.  

This visualization effectively demonstrates the **growth trends and correlation** between **education and economic prosperity** across different regions over time.

---
