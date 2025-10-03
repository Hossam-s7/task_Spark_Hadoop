1. Read the CSV file provided into a Spark DataFrame.

2. Count the number of males and females who had their Cabin as null.

3. Find the average ages of passengers.

4. Fill in the missing age values with this average value.

5. Save the output to a CSV file in HDFS (depi_folder).

6. Count the total number of passengers who survived and those who did not.

7. Find the top 5 most common embarkation ports among passengers.

8. Calculate the survival rate by passenger class (Pclass).

9. Determine the maximum, minimum, and average fare paid by passengers.

10. Write a Spark job to count the number of passengers in each age group (e.g., 0–18, 19–35, 36–60, 60+).

11. Create a new directory in HDFS called titanic_lab and list its contents.

12. Upload the Titanic dataset from your local machine to the titanic_lab directory in HDFS.

13. Use chmod command to change the permissions of the Titanic dataset file to 777 (full permissionsfor all)

14. Use-cat to display the first 20 lines of the Titanic dataset stored in HDFS.

15- Move the processed output file from titanic_lab to a new directory in HDFS called titanic_results using hdfs dfs -mv.
