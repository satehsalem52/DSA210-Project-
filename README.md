# DSA210-Term-Project-Fall-2024

## Motivation
While brainstorming ideas for this project, many aspects of my personal data came into my head that I wanted to explore and learn about. Then it hit me: the most anxiety-inducing thing for me lately has been receiving university emails. Each email could bring anything from an exam grade release to an assignment deadline or other important updates. This made me realize that analyzing my email patterns could help me understand when I receive the most emails, who sends them, and how to manage them more effectively, among other patterns. By doing this, I hope to reduce the stress of constantly checking my inbox by predicting when these stress-inducing emails will be sent.

## Project Idea

The aim of this project is to analyze university emails and extract interesting insights that would help students manage their inboxes more effectively. Such analysis could provide information like
- **Best time of day** to check emails, to avoid unnecessary inbox distractions.
- **Most frequent senders** of emails, helping to identify key contacts or departments.  
- **Peak weeks** in a semester for receiving emails, allowing students to prepare for high-volume periods.  
- **Email categorization** by subject or sender type, such as academic versus extracurricular. 
- **Response time trends**, analyzing how quickly emails are typically addressed.  
- **Frequency of emails by weekday**, showing if there are days of the week that are more busy than others. 

In highlighting these trends, this work may position students to take their email management to new heights: allowing students to plan better their time, reduce the email related stress, and adopt more strategic vision towards their inbox. It will probably also give several worthy recommendations to the university administrations in terms of improvement perspectives on email communication at student level.

---

## Dataset Description

This project uses a dataset of university emails collected from Google Takeout and Thunderbird. The dataset includes valuable information such as:  
- **Email timestamps** to track when emails are sent and received.  
- **Sender details** to identify frequent senders and key contacts.  
- **Subject lines** (optional for analysis) to categorize and understand email content.  
- **Day and week metadata** for analyzing email trends across specific times of the semester.

---

## Plan
1. **Data Extraction**  
   Use Python to extract email data from text files exported via Google Takeout and Thunderbird.

2. **Data Cleaning**  
   Process the data to extract relevant fields such as timestamps and sender information.

3. **Data Analysis**  
   Use Python libraries like Pandas to:
   - Analyze the frequency of emails by time of day
   - Identify the busiest weeks in the semester
   - Find the most frequent senders

4. **Data Visualization**  
To effectively analyze the university email dataset, various visualizations will be created to uncover patterns and trends. These visualizations will include bar charts, line graphs, and heatmaps to represent findings such as the busiest email hours, most frequent senders, and peak weeks in the semester.

The visualizations will be developed using Python libraries such as Matplotlib and Seaborn for their powerful and customizable plotting capabilities. By using these tools, the data will be presented in a clear, engaging, and informative manner to help understand email trends effectively.

All visualizations will be included in a dedicated Jupyter Notebook.

---

## Predictions
1. The most emails are received between **12:00 PM and 2:00 PM**.  
2. The busiest weeks for email activity are between **Week 7 and Week 10** of the semester.  
3. Since I am a CS student, most of my emails will likely be from CS professors and academic advisors, particularly related to coursework, assignments, and project updates.  
4. Email traffic is generally lower on weekends compared to weekdays, with the highest volume occurring midweek (e.g., Tuesdays and Wednesdays).  

---
## Findings


---
## Limitations and Future Work


