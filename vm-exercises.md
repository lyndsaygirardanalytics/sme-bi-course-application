# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The two exercises should not replicate the exact actions shown in your screencast. The goal of exercises is for learners to apply what was learned in the screencasts to new problems or situations. This is best pedagogical practice for retaining and building skills. For example, this can be done by using another dataset between screencasts and exercises or focusing on a different portion of the dataset.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/introduction-to-power-bi/getting-started-with-power-bi?ex=14) from Introduction to Power BI. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners.

## 1st VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*Perform a group-by transformation using the correct grouping operation to prepare for aggregate analysis and linkage with another dataset.*

#### Context

*The “Group By'' operation is very useful in aggregating data to summarize information within your dataset. In this exercise, you will revisit the drug_adminsitrations dataset to analyze the total number of drug administrations by date.*

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- Step 1: Create a duplicate query of the drug_administrations and rename the query drug_administration_by_date.
- Step 2: Perform a Group By table transformation to count rows by the medication_administration_date column. Label the new column name “Total Administrations”.
- Step 3: Filter out any null values for missing dates.
- Step 4: In the View tab of the Excel Power Query ribbon, view the column profile for Total Administrations.

#### Exercise question:
How many unique days had 1 or more drug administrations?
A) 365
B) 554 *ANSWER
C) 555
D) 6


#### End goal:
![Ex1_Image](https://github.com/lyndsaygirardanalytics/sme-bi-course-application/assets/125575969/e89eacca-0704-4ed0-a33b-6e8f5c00a4ab)


## 2nd VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-2-intial.twbx` or `ex-2-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-2-sol.twbx` or `ex-2-sol.pbix`

#### Learning Objective

*Merge two queries together using a left join to match on a common column. Practice calculating custom column and sorting.*

#### Context

*With the drug_administrations_by_date query now summarized by unique date, it’s primed and ready to be joined up with our dailycensus dataset. Since both queries can now be matched on the date column, you will combine the two using a Merge Queries step with a left join. You will finish off this exercise by adding a custom calculated column that combines information from both queries*

#### Steps to be executed by the student (max 6)

- Step 1: With the drug_administration_by_date query open, set up a query merge with dailycensus_2230 using medication_administration_date and effective_date as the matching columns. Join using the defaulted Left Outer join.
- Step 2: Click the Expand button on the newly created dailycensus column. Expand to just include the patient_days column from dailycensus values. You can leave the original column name as prefix.
- Step 3: Add a Custom Calculated column by dividing administrations over patient days and multiplying by 1000. Label the new column “drug administrations per 1000 pt days”.
- Step 4: Transform the data type of the new column to decimal number.
- Step 5: Sort drug administrations per 1000 pt days in descending order.

#### Exercise question:
What was the highest observed Total Administrations per 1000 patient days? Rounded to 2 digits.
A) 5.53
B) 6.17
C) 846.60
D) 8.27 *ANSWER


#### End goal:

![Ex2_Image](https://github.com/lyndsaygirardanalytics/sme-bi-course-application/assets/125575969/8dc3ac54-efe9-486f-a76f-d1c28fbfd090)


