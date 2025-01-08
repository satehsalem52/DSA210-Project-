# DSA210-Term-Project-Fall-2024

## Motivation
While brainstorming ideas for this project, many aspects of my personal data came into my head that I wanted to explore and learn about. Then it hit me: the most anxiety-inducing thing for me lately has been receiving university emails. Each email could bring anything from an exam grade release to an assignment deadline or other important updates. This made me realize that analyzing my email patterns could help me understand when I receive the most emails, who sends them, and how to manage them more effectively, among other patterns. By doing this, I hope to reduce the stress of constantly checking my inbox by predicting when these stress-inducing emails will be sent.

## Project Idea

The aim of this project is to analyze university emails and extract interesting insights that would help students manage their inboxes more effectively. Such analysis could provide information like
1. **Identifying the Most Frequent Email Senders**  
   By analyzing the sender information, we aim to identify which individuals, departments, or automated systems send the most emails. This information will help prioritize responses, highlight key contacts, and organize the inbox more effectively.

2. **Determining the Best Times to Check Emails**  
   By examining email timestamps, we will analyze trends in email activity throughout the day and week. This analysis will help identify optimal times for students to check their inboxes, minimizing distractions and improving time management.

3. **Analyzing Monthly and Weekly Trends**  
   By studying email frequency across months and weeks, we aim to identify periods of high activity, such as midterms, finals, or important administrative deadlines. Understanding these patterns can help students anticipate and prepare for high-email periods.

4. **Categorizing Emails by Topic and Sender Type**  
   By extracting keywords from subject lines and analyzing sender types, we plan to categorize emails into groups such as academic, administrative, or extracurricular. This categorization will assist in organizing emails and prioritizing important messages.

5. **Visualizing Hourly Distribution**  
   By breaking down email activity by hour, we aim to determine which times of day are the busiest for receiving emails. This insight will help students better manage their time and set up inbox filters or rules for non-critical emails.

6. **Exploring Course-Specific Trends**  
   By analyzing email data related to specific courses, we aim to identify which courses generate the most email communication. This information will help students prioritize coursework-related emails and manage their academic workload more effectively.


In highlighting these trends, this work may position students to take their email management to new heights: allowing students to plan better their time, reduce the email related stress, and adopt more strategic vision towards their inbox. It will probably also give several worthy recommendations to the university administrations in terms of improvement perspectives on email communication at student level.

---

## Dataset Description

The dataset for this project was collected from Google Takeout and Thunderbird, covering the period from Monday, 29 August 2022, to Wednesday, 20 November 2024. It contained valuable fields that facilitated the analysis:

- **Email Timestamps**  
  The exact date and time when emails were sent or received, allowing for the analysis of patterns such as peak hours and days for email traffic.  

- **Sender Details**  
  Information about who sent the email, including both the sender's name and email address, which helps identify frequent senders and key contacts.  

- **Subject Lines**  
  Email subjects provide context for categorizing and understanding the content of the emails, such as assignments, deadlines, or general announcements.  

- **Day, Month, and Year Metadata**  
  Extracted components of the date, allowing analysis of trends across specific days, months, and years.  

- **Weekday Information**  
  The day of the week (e.g., Monday, Tuesday) for analyzing weekly trends in email activity.  

- **Time Details**  
  Hour, minute, and second-level granularity to identify peak email times during the day.  

The dataset contains all the necessary fields to uncover patterns in email communication and provide actionable insights for better inbox management.


---

## Plan

### 1. **Data Extraction**
- Use Python to extract email data from `.mbox` files exported via Google Takeout and Thunderbird.
- Focus on retrieving key fields such as:
  - **Timestamps:** Date and Time of emails.
  - **Sender Details:** Name and Email Address.
  - **Subject Lines**
  - **Metadata:** Weekday, Hour, and other time components.

### 2. **Data Cleaning**
- Preprocess the extracted data to ensure accuracy and usability:
  - Parse and format timestamps to extract components such as Day, Month, Year, Hour, Minute, and Second.
  - Clean and separate the sender field into **Name** and **Email Address** using regular expressions.
  - Handle missing or invalid data by assigning placeholder values or excluding incomplete records.

### 3. **Data Analysis**
Use Python libraries like Pandas to perform the following analyses:

- **Frequency of Emails by Time of Day**  
  Analyze the number of emails received at different hours to identify daily patterns in email activity.

- **Busiest Weeks and Months in the Semester**  
  Identify the weeks and months with the highest email volume to uncover trends related to academic and administrative cycles.

- **Most Frequent Email Senders**  
  Aggregate email counts by sender to determine the most active individuals or departments.

- **Categorization by Topics and Courses**  
  Use subject lines to classify emails into categories such as academic, administrative, or extracurricular.  
  Extract course-related codes (e.g., CS204, MATH101) to analyze course-specific trends.

- **Email Trends Across Years**  
  Compare email activity across different years to observe changes in patterns over time.

### 4. **Data Visualization**
Create insightful visualizations using Python libraries such as Matplotlib, Seaborn, and WordCloud:

- **Bar Charts**  
  - Top 10 most frequent email senders.  
  - Hourly distribution of emails to identify peak email hours.  
  - Most active courses based on email volume.

- **Line Graphs**  
  - Monthly email trends to visualize fluctuations over time.

- **Heatmaps**  
  - Hourly and weekday trends to uncover when emails are typically sent during the week.

- **Word Cloud**  
  - Common keywords in email subject lines to identify dominant themes.

Each visualization will be carefully designed to effectively communicate the trends and insights discovered during analysis.

### 5. **Output and Documentation**
- Save the cleaned and analyzed data into a CSV file for further reference or reuse.
- Include all visualizations in a well-documented **Jupyter Notebook** for ease of understanding and reproducibility.

This plan ensures a structured approach to analyzing university emails and provides actionable insights for improved email management.

---

## Predictions

1. The majority of emails will be received during **morning hours (e.g., 9:00 AM to 11:00 AM)**, aligning with the start of academic and administrative workdays.  
2. The most frequent email senders will likely be **automated systems** (e.g., noreply addresses) and **key university departments** such as academic advisors, course coordinators, or housing services.  
3. Email activity will be significantly lower on **weekends**, with the highest traffic occurring on **weekdays**, particularly midweek (e.g., **Tuesday and Thursday**).  
4. Keywords in email subject lines will predominantly relate to **coursework, deadlines, and exams**, with common terms like "submission," "exam," and "grades."  
5. Emails related to **Computer Science** (e.g., CS204 or CS300) will dominate the dataset, reflecting the academic workload and communication frequency from these courses.

---
## Findings

### 1. **Most Frequent Email Senders**
- Automated systems like **noreply.sucourse@sabanciuniv.edu** and **noreply@sabanciuniv.edu** are the top email senders, accounting for a large portion of the inbox traffic.  
- Key university departments such as **housing services** (yurtlar@sabanciuniv.edu) and **academic offices** also contribute significantly.

### 2. **Peak Email Times**
- The busiest hour for receiving emails is **10:00 AM**, aligning with the start of academic and administrative operations.  
- This spike is also influenced by **GazeteSU**, which sends daily messages at exactly **10:30 AM** every morning, contributing significantly to the volume of emails during this hour.  
- Email activity gradually decreases in the evening and is lowest late at night.

### 3. **Weekly Trends**
- **Midweek (Tuesday and Thursday)** are the busiest days for email activity, while **weekends** show significantly lower traffic.

### 4. **Monthly and Yearly Trends**
- Email activity spikes in **May** and **December**, likely corresponding to midterms, finals, and semester-end deadlines.  
- Comparisons across years show consistent activity patterns in these months, with minor fluctuations.

### 5. **Course-Specific Trends**
- Certain courses, such as **CS204** and **SPS101**, dominate email traffic, reflecting high communication needs for these courses.  
- Higher email volumes for some courses, such as CS204 and MATH203, were influenced by these courses being taken multiple times during the analyzed period.

### 6. **Keywords in Subject Lines**
- Common keywords like **"submission," "exam," "grades,"** and **"assignment"** indicate the academic nature of most emails.  
- The word cloud highlights a focus on deadlines and coursework, emphasizing the importance of effective email management for academic success.

### 7. **Heatmap Analysis**
- The heatmap shows a clear pattern: the busiest hours for emails are between **9:00 AM and 11:00 AM** on weekdays, particularly on **Monday through Thursday**.  
- The lowest activity occurs on **weekends**, with minimal emails sent late at night or early morning.

## Implications of Findings
- These insights can help students identify **optimal times to check emails** (e.g., around 10 AM on weekdays).  
- Understanding course-specific trends allows students to better prioritize and organize their inboxes for high-traffic courses.  
- Recognizing peak periods of email activity (e.g., May and October) helps students prepare for heavy academic and administrative workloads.

---

## Limitations
- **Bias in Dataset**: The dataset reflects personal email patterns, which may not generalize to other students or departments.
- **Categorization Challenges**: Extracting keywords and categorizing emails was limited by inconsistent subject lines and missing course information.



