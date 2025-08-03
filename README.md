
# 📊 Student Performance Dashboard – Power BI

This project presents an interactive Power BI report for visualizing and analyzing student academic performance across various subjects and classes. It is designed to assist educators in identifying performance trends, grade distributions, and top performers.

---

## ✅ Features

* Interactive dashboard for monitoring student progress
* Dynamic calculation of total marks, average, and grades
* Visual breakdown of marks by subject
* Grade distribution analysis
* Highlight of top-performing students
* Filtering by class, term, and subject

---

## 🛠 Technologies Used

* Power BI Desktop
* DAX (Data Analysis Expressions)
* Power Query (for data transformation)
* Excel/CSV as data source

---

## 📌 Report Visuals & Components

1. 📋 Student Marks Table

* Fields: Student Name, English, Maths, History, Science, Total Marks, Average Marks, Grade
* Shows row-wise performance metrics

2. 📊 Subject-wise Bar Chart

* Visual: Stacked Column or Clustered Column Chart
* Shows average or total marks per subject

3. 🥧 Grade Distribution Pie Chart

* Displays the number of students in each grade category (A to F)

4. 🏆 Top Performers Bar Chart

* Highlights students with the highest total marks
* Sorted in descending order

5. 🎛 Filters (Slicers)

* Class
* Exam Term
* Subject (if subjects are unpivoted in Power Query)

---

## 📈 DAX Calculations

Basic Measures Used:

```dax
Total Marks = [English] + [Maths] + [History] + [Science]

Average Marks = DIVIDE([Total Marks], 4)

Grade = 
SWITCH(TRUE(),
    [Average Marks] >= 90, "A",
    [Average Marks] >= 75, "B",
    [Average Marks] >= 60, "C",
    [Average Marks] >= 45, "D",
    "F"
)
```

---

## 🧮 Data Transformation (Optional)

To analyze subject-wise trends using a single visual:

1. Open Power Query Editor
2. Select subject columns (English, Maths, etc.)
3. Right-click → Unpivot Columns
4. Resulting format:
   \| Student | Subject | Marks |

---

## 📌 Final Output

An interactive report showing:

* Subject-wise scores
* Grade distribution ratios
* Top performers by class
* Filters to drill down by class, subject, or exam term

---

## 🗃 Example

You can find the .pbix file and sample dataset in the repository for demo and customization.

---


