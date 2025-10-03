# Titanic Data Analysis with Spark & Hadoop  

## 📌 Overview  
This project demonstrates how to use **Apache Spark** and **Hadoop HDFS** to perform data analysis on the Titanic dataset.  
The tasks include data preprocessing, survival analysis, handling missing values, saving results to HDFS, and performing file operations using Hadoop commands.  

---

## 🛠 Technologies Used  
- **Python 3.11**  
- **PySpark**  
- **Pandas**  
- **Hadoop 3.3.6**  
- **HDFS**  

---

## 📂 Project Workflow  

1. **Load Data**  
   - Read the Titanic dataset (`titanic.csv`) into a Spark DataFrame.  

2. **Null Cabin Analysis**  
   - Count the number of males and females with missing cabin information.  

3. **Age Processing**  
   - Calculate the average age of passengers.  
   - Fill missing age values with the computed average.  

4. **Save Processed Data**  
   - Write the cleaned dataset to **HDFS** under `/depi_folder/titanic_output`.  

5. **Survival Analysis**  
   - Count total survivors and non-survivors.  
   - Calculate survival rates by passenger class (`Pclass`).  

6. **Embarkation Ports**  
   - Find the top 5 most common embarkation ports.  

7. **Fare Analysis**  
   - Determine the **maximum, minimum, and average fares**.  

8. **Age Group Distribution**  
   - Categorize passengers into age groups: `0–18`, `19–35`, `36–60`, `60+`.  

9. **HDFS Operations**  
   - Create a directory `/titanic_lab`.  
   - Upload the Titanic dataset to HDFS.  
   - Change file permissions using `chmod 777`.  
   - Display first 20 lines of the dataset with `hdfs dfs -cat`.  
   - Move processed results to `/titanic_results`.  

---

## ▶️ How to Run  

1. **Start Hadoop & HDFS**  
   ```bash
   start-dfs.sh
   start-yarn.sh
   ```

2. **Run Spark Job**  
   ```python
   spark-submit titanic_spark_job.py
   ```

3. **HDFS Commands Examples**  
   ```bash
   hdfs dfs -mkdir -p /titanic_lab
   hdfs dfs -put titanic.csv /titanic_lab/
   hdfs dfs -chmod 777 /titanic_lab/titanic.csv
   hdfs dfs -ls /titanic_lab
   ```

---

## 📊 Sample Results  

- **Males with null Cabin**: 470  
- **Females with null Cabin**: 217  
- **Average Age**: ~29.7 years  
- **Survival Counts**: 342 survived, 549 did not  
- **Top Embarkation Port**: Southampton (S)  

---

## 📁 Project Structure  

```
├── Spark_and_Hadoop_Lab.ipynb   # Jupyter notebook with full workflow
├── titanic.csv                  # Titanic dataset
├── README.md                    # Project documentation
└── output/                      # Processed results saved in HDFS
```
