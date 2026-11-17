Student Academic Performance Analytics Dashboard

An interactive data analytics project that explores how study hours and attendance relate to student marks, compares performance across academic programs, and presents the findings in a single exportable Plotly dashboard.

Built in Python (Google Colab) with pandas, NumPy, Matplotlib and Plotly.
Overview

The goal of this project is to turn raw academic data into clear, decision-ready insights. It answers questions such as:

Does studying more actually lead to higher marks?
How strongly is attendance linked to performance?
Which program (BCA, BSc, BCom, BBA) performs best on average?
What share of students score 60 or above?
Is there any trend in marks across assessment dates?

The notebook ends with a combined 2 x 2 interactive dashboard exported as a standalone HTML file that can be shared and opened in any browser.

Features
Dataset generation and structural inspection (shape, dtypes, descriptive statistics)
Correlation analysis with an annotated heatmap
Program-wise aggregation (average study hours, attendance, marks, student count)
Static charts with Matplotlib (scatter, bar, histogram)
Interactive charts with Plotly (hover details, colour by program, bubble size by attendance)
Linear trend line showing marks gained per extra study hour
Insight-driven chart titles computed dynamically from the data
One-click export of the dashboard to student_performance_dashboard.html
Auto-generated written reflection summarising the findings
Dataset

The dataset is synthetically generated inside the notebook (30 students), so the project runs without any external files.

Column	Type	Description
Student	string	Student first name
Study_Hours	float	Average study hours per day (1.0 to 9.0)
Attendance	int	Attendance percentage (50 to 100)
Marks	int	Assessment marks (30 to 100)
Program	category	One of BCA, BSc, BCom, BBA
Assessment_Date	datetime	Business-day dates starting from 2026-02-02

Attendance is modelled as a function of study hours, and marks as a function of both study hours and attendance, each with random noise. No random seed is set, so values (and exact results) change on every run.

Tech Stack
Python 3
pandas: data manipulation and aggregation
NumPy: random data generation and trend-line fitting
Matplotlib: static visualisations
Plotly (plotly.express, plotly.graph_objects, make_subplots): interactive charts and dashboard
Google Colab : runtime environment
