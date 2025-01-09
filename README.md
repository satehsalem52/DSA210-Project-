# DSA210-Term-Project-Fall-2024

## **Table of Contents**
1. [Motivation](#motivation)
2. [Project Idea](#project-idea)
    - [Objectives](#objectives)
3. [Dataset Description](#dataset-description)
4. [Plan](#plan)
5. [Predictions](#predictions)
6. [Findings](#findings)
    - [Most Frequent Email Senders](#1-most-frequent-email-senders)
    - [Course-Specific Trends](#2-course-specific-trends)
    - [Peak Email Times](#3-peak-email-times)
    - [Weekly Trends](#4-weekly-trends)
    - [Monthly and Yearly Trends](#5-monthly-and-yearly-trends)
    - [Keywords in Subject Lines](#6-keywords-in-subject-lines)
7. [Implications](#implications)
8. [Limitations](#limitations)
9. [Future Work](#future-work)

---

## **Motivation**

University life comes with a flood of responsibilities, and for me, emails have been a constant source of stress. Whether it’s exam grades, assignment deadlines, or important announcements, the sheer volume of emails I receive can be overwhelming. These emails often come at unpredictable times, and staying on top of my inbox has become a challenge.

This project emerged from my personal need to bring order to this chaos. I wanted to understand my email patterns when they arrive, who sends them, and what they’re about so I could manage my inbox more effectively. By doing so, I hoped to reduce the stress of constantly checking for important updates and instead approach my inbox strategically.

---

## **Project Idea**

This project focuses on analyzing my university emails to extract actionable insights that could make managing my inbox less stressful. Through this analysis, I aim to uncover trends and patterns that would allow me to better prioritize and organize my email communication.

### **Objectives**

1. **Identifying the Most Frequent Email Senders**: 
   - Understand which individuals, departments, or automated systems dominate my inbox.
   - Highlight key senders to prioritize responses.

2. **Exploring Course-Specific Trends**:
   - Determine which courses generate the most email traffic.
   - Identify patterns related to coursework, deadlines, and professor announcements.

3. **Determining the Best Times to Check Emails**: 
   - Pinpoint peak hours for email activity to minimize distractions during the day.

4. **Analyzing Monthly and Weekly Trends**:
   - Highlight peak periods like midterms, finals, or administrative deadlines.

5. **Visualizing Hourly Distribution**:
   - Understand which times of day are busiest for email traffic.

6. **Categorizing Emails by Topic and Sender Type**:
   - Group emails into categories (e.g., academic, administrative, extracurricular) to simplify inbox management.

---

## **Dataset Description**

The dataset consists of my personal university emails collected via Google Takeout and Thunderbird, spanning from **Monday, 29 August 2022, to Wednesday, 20 November 2024**. It reflects the challenges I face managing email communication throughout my academic journey.

Here are the key fields I worked with:

- **Email Timestamps**: 
  Tracks the exact date and time emails were sent or received.

- **Sender Details**:
  Includes sender names and email addresses, helping identify frequent senders.

- **Subject Lines**:
  Provides context for categorizing emails (e.g., assignments, deadlines, announcements).

- **Day, Month, and Year Metadata**:
  Enables trend analysis across specific days, months, and years.

- **Weekday Information**:
  Highlights patterns during weekdays and weekends.

- **Time Details**:
  Includes hour, minute, and second information to pinpoint peak email times.

**Note**: Some courses, like **CS204** and **MATH203**, have higher email volumes because I took them multiple times. This reflects the iterative nature of my academic journey and the challenges associated with retaking courses.

---

## **Plan**

### **1. Data Extraction**
- Extract email data from `.mbox` files exported via Google Takeout and Thunderbird.
- Retrieve key fields such as:
  - Timestamps (Date and Time)
  - Sender Details (Name and Email Address)
  - Subject Lines
  - Metadata (Weekday, Hour, etc.)

### **2. Data Cleaning**
- Preprocess the data to ensure accuracy:
  - Parse timestamps into day, month, year, hour, etc.
  - Clean sender fields to extract names and email addresses.
  - Handle missing data by assigning placeholders or excluding incomplete records.

### **3. Data Analysis**
- Use Python (Pandas) to perform:
  - **Hourly Trends**: Analyze emails received by hour.
  - **Weekly and Monthly Trends**: Identify spikes in email activity.
  - **Frequent Senders**: Highlight top contributors to email volume.
  - **Course-Specific Analysis**: Determine which courses generate the most emails.
  - **Yearly Comparisons**: Compare email activity across years.

### **4. Data Visualization**
- Create visualizations using Matplotlib, Seaborn, and WordCloud:
  - Bar charts for frequent senders and hourly distributions.
  - Line graphs for monthly trends.
  - Heatmaps for hourly/weekday trends.
  - Word clouds for subject line keywords.

### **5. Output**
- Save processed data into a CSV file.
- Document the analysis and visualizations in a Jupyter Notebook.

---

## **Predictions**

1. Most emails will arrive during **morning hours (e.g., 9:00 AM to 11:00 AM)**.
2. Frequent senders will include **noreply systems** (e.g., SUCourse) and key university departments.
3. Email traffic will peak on **Tuesdays and Thursdays** and drop significantly on weekends.
4. Common subject line keywords will include terms like **"submission," "exam," "grades,"** and **"assignment."**
5. Courses like **CS204** and **MATH203** will dominate email volume.

---

## **Findings**

### 1. **Most Frequent Email Senders**
- Automated systems like **noreply.sucourse@sabanciuniv.edu** dominated my inbox.
- Investigating further, I found these emails were often announcements from professors for courses I’m enrolled in.
- Departments like housing services and academic offices were also significant contributors.

### 2. **Course-Specific Trends**
- Courses like **CS204** and **SPS101** generated the highest email traffic, primarily related to assignments and deadlines.
- Many of these emails were tied to **noreply.sucourse@sabanciuniv.edu**, showing the connection between frequent senders and course communication.

### 3. **Peak Email Times**
- The busiest hour was **10:00 AM**, heavily influenced by daily messages from **GazeteSU** sent at **10:30 AM**.
- Email activity decreased steadily in the evening, reaching its lowest late at night.

### 4. **Weekly Trends**
- **Tuesdays and Thursdays** were the busiest days, while weekends saw significantly fewer emails.

### 5. **Monthly and Yearly Trends**
- Activity peaked in **May** and **December**, coinciding with midterms, finals, and semester-end deadlines.
- Consistent trends were observed across 2022, 2023, and 2024.

### 6. **Keywords in Subject Lines**
- The most common keywords included **"submission," "exam," "grades,"** and **"assignment,"** emphasizing the academic focus of most emails.

---

## **Implications**

1. **Optimized Inbox Management**: 
   - Knowing that email traffic peaks around **10:00 AM**, I can schedule email checks during this window to stay updated without distractions.
   - Avoiding late-night inbox checks can help create better boundaries between academic and personal time.

2. **Course Prioritization**: 
   - Identifying courses like **CS204** and **SPS101** as high-traffic sources helps me focus on these emails for better academic organization.
   - Recognizing that many course-related emails come from SUCourse allows me to filter and prioritize announcements effectively.

3. **Stress Reduction**: 
   - Anticipating peak periods, such as **May** and **December**, helps me prepare for high email traffic and manage my academic workload more efficiently.
   - Understanding weekly and hourly patterns allows me to create a more structured approach to handling my inbox, reducing the anxiety of unexpected emails.

4. **Improved Time Management**: 
   - By focusing on high-traffic times, such as **Tuesday mornings**, I can allocate specific slots in my schedule to process emails without interrupting other tasks.

5. **University Recommendations**: 
   - These insights could guide universities to consolidate emails into fewer, more structured announcements, reducing email overload for students.
   - Universities might also consider scheduling important emails outside of peak times to ensure better visibility and engagement.

---

## **Limitations**

- **Personal Dataset**: The findings reflect my personal email patterns and may not generalize to others.
- **Keyword Extraction**: Inconsistent subject lines made categorization challenging.

---

## **Future Work**

1. Expand the dataset to include anonymized emails from other students.
2. Use NLP to automate email categorization.
3. Analyze response times to identify bottlenecks in email management.
4. Provide actionable recommendations to the university for better communication practices.
