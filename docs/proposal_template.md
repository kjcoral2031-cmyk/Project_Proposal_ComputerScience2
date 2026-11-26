# 📌 Project Proposal (Draft)

## 📝 Project Title  
Student Academic Grade and Performance Tracker

---

## 🔍 Problem Statement  
Students and class officers often struggle to organize and analyze academic performance when grades across multiple subjects and sections are scattered across different platforms or sheets. Without a quick way to look up student records, update scores, and summarize class or subject averages, it is difficult to identify low-performing subjects early or compare performance across sections. Using the `students.json` dataset—which stores student IDs, names, sections, and subject grades—this application solves that problem by centralizing student grade management and providing instant statistical summaries.

---

## 🎯 Project Objectives  
**Objective 1: To store, manage, and analyze student grade records from the `students.json` dataset using full Create, Read, Update, and Delete (CRUD) operations.

**Objective 2: To help users gain meaningful academic insights, including individual student averages, per-subject class averages, section comparisons, and highest/lowest grades.

**Objective 3: To apply Python programming concepts—such as functions, loops, arrays/lists, input validation, and JSON file handling—in building a reliable data application.

---

## ⚙️ Planned Features  
**Feature 1 (Starter Idea): Compute and display each student's overall average grade and overall class/subject averages from `students.json`.

**Feature 2 (Starter Idea): Search and filter student records by Student ID, name, or section to view their subject grades.

**Feature 3 (Additional Feature): Add a new student record (ID number, name, section, and subject grades) with input validation and save it persistently to `students.json`.

**Feature 4 (Additional Feature): Update or delete an existing student's section or subject grades by entering their Student ID.

**Feature 5 (Additional Feature): Generate a performance summary report showing the highest and lowest scores per subject, section averages, and a visual bar chart comparison.

---

## ⌨️ Planned Inputs and Outputs  

- **Inputs**
  * Menu choice (`0–6`) to navigate features
  * Student ID number, student name, and section (for adding, searching, editing, or deleting records)
  * Subject names and numerical grades (`0–100`) when adding or updating student scores
  * Confirmation prompt (`Y/N`) before deleting a record
- **Outputs**
  * Formatted table displaying student IDs, names, sections, and individual subject grades
  * Calculated student general averages and class averages per subject
  * Summary statistics highlighting the highest and lowest grades, top-performing section, and a visual bar chart comparing subject averages 

---

## 🧠 Logic Plan  
The Student Academic Grade and Performance Tracker starts by loading existing student records (student ID, name, section, and subject grades) from data/students.json into a list in memory. If the file is empty or missing, the program starts safely with an empty list so it does not crash.

Once loaded, a loop displays the main menu repeatedly until the user chooses to exit. Depending on the user's menu choice, the program runs a specific action:

- View and Search/Filter: Loops through the stored records to display all students or find matching entries by Student ID, name, or section.

- Add Record: Collects the student ID, name, section, and subject grades, checks that inputs are valid (non-empty fields, unique ID, and grades within 0-100), appends the record to the list, and saves the updated list back to data/students.json.

- Edit Record: Searches for the matching Student ID, lets the user update the section or subject grades with input validation, and writes the updated data back to data/students.json.

- Delete Record: Looks up the record by Student ID, asks for confirmation (Y/N) to avoid accidental deletions, removes the record from the list, and saves the changes to data/students.json.

- Summary and Chart: Iterates through the records and grade values to compute student averages, subject averages, highest and lowest grades, and section or subject comparisons, displaying both a text summary and a visual bar chart.

### Pseudocode  
Load students.json file

Display menu of features

If user chooses "1", display all student records

If user chooses "2", search or filter student records by ID, name, or section

If user chooses "3", add a new student record with validated details and save to students.json

If user chooses "4", update an existing student record or subject grades and save to students.json

If user chooses "5", delete a student record after confirmation and save to students.json

If user chooses "6", compute averages, highest/lowest grades, and display the summary and chart

Repeat until user chooses "0" to exit program


### Flowchart
                    [ Start ]
                        |
                        v
           [ Load students.json ]
                        |
                        v
         +---> [ Display Menu ] <----+
         |              |            |
         |      [ Get User Choice ]  |
         |              |            |
         |    +---------+---------+  |
         |    v         v         v  |
         | [View /   [Add /    [Summary|
         |  Filter]  Edit / Del] & Chart]|
         |    |         |         |  |
         |    |         v         |  |
         |    |   [Validate &     |  |
         |    |    Save JSON]     |  |
         |    |         |         |  |
         +----+---------+---------+--+
                        |
                 (Choice == "0")
                        v
                     [ End ]
                     

---

## 📂 GitHub Repository Link  
Paste your GitHub repository link here:  
https://github.com/kjcoral2031-cmyk/Project_Proposal_ComputerScience2`  

---
