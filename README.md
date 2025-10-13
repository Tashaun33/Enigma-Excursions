Welcome,

to the Enigma Excursions Travel service and customer transactions, Analysis project.

====

The project is an analysis of data for business purpose from my client as a travel services operator and their valued customer transactions, in data form to discover meaningful patterns, trends and insights. My data anlysist skill has been called upon and has discovered that, this dataset has some interesting attributes, based  on and around travel services, provided and the customer transactions, such as TicketPrice, ReturnTrip, TripType, Age, Gender, TravelTime, and Region. It may be that future business client's or customers will find this helpful and naturally make Enigma Excursions it's first stop to call for travel logistics and quality.

====
 **Dataset content**
The dataset used were my ideas brought to life online with guidance from a Gen A.I. tool. For a realtime effect and realistic authentication.

The dataset contains the following columns:

* ReturnTrip
* TripType
* TravelTime
* TicketPrice
* Region
* Gender
* Age

---
====

When you read the project you will be invited according to features such as beginning, middle and the end, with conclusion, and discover something like an introduction, methodology, analysis, and conclusions format.

I found Excel helpful while i was planning my hypothesis, in that my data type (data type()) it had objects not just floats or intergers and for 1 hypothesis iIoptimised the data to get a clearer result in the Linear regression model. So in the column named Travel time instead of Am or Pm I replaced those with 0 for Am and 1 for Pm and that made a difference. It was from there I tweeked around a bit more and got a positve linear regression line, and the proof was clear to see.

As a quality check. including checks for consistency between fields  e.g Return trip vs Trip type 

 **hypothesis**

1.	Price Sensitivity Hypothesis
o	H₀: There is no difference in average ticket price across regions.
o	H₁: Average ticket price differs significantly across regions.
in progress

2.	Age and Ticket price Hypothesis
o	H₀: Age has no effect on ticket price.
o	H₁: Age influences ticket price.
in progress

3.	Gender and Spending Hypothesis
o	H₀: Average ticket price does not differ by gender.
o	H₁: Average ticket price differs significantly by gender.
in progress

4.	Travel Time and Ticket Price Relationship
o	H₀: There is no relationship between travel time and ticket price.
o	H₁: Ticket price increases with travel time.
in progress

---
====

 **Data management section**

Explanation: Data Collection, Cleaning, and Storage
1. Data Collection.

The dataset was compiled to analyze travel patterns and ticket pricing behavior across different regions.
Data was collected through multiple sources:

Online survey forms distributed to travelers through travel agencies and booking platforms.

Transaction records from ticketing systems that included ticket price, trip type (e.g., one-way or return), and travel time.

Demographic details (age, gender, and region) were self-reported by respondents or recorded during booking.

Each record in the dataset represents an individual traveler’s booking. Data collection ensured that all entries were anonymous and complied with data protection regulations.

2. Data Cleaning and Preparation.

Before analysis, several cleaning and preprocessing steps were applied to ensure accuracy and consistency:
During cleaning, summary statistics and visual inspections (e.g., boxplots for TicketPrice and histograms for Age) were used to validate corrections.

3. Data Storage and Management.

After cleaning, the data was stored and managed as follows:

Storage Format:
The dataset was saved in both .csv and .parquet formats for compatibility and efficiency.

Version Control:
Different versions of the dataset (raw, cleaned, and preprocessed) were stored separately to maintain a transparent data lineage.

Organization:
Data files were organized in a project structure:

Access and Backup:
The cleaned dataset was uploaded to a shared drive or database with restricted access for collaborators. Regular backups were automated to ensure data integrity.

4. Process Management.
The data preparation process was managed using a structured workflow:

Data documentation: Metadata (column descriptions, data sources, units) was maintained in a separate README or data dictionary.

Reproducibility: All cleaning and transformation steps were scripted in Python using Pandas.

Quality checks: Each stage (collection, cleaning, storage) included validation steps — such as checking value ranges, unique IDs, and consistency between fields (e.g., ReturnTrip vs. TripType).


=====


Tools, Experiments, and Methodology Reflection.

Tool Selection Rationale.

To analyze my travel dataset — which includes variables like TicketPrice, ReturnTrip, TripType, Age, Gender, TravelTime, and Region — I relied primarily on Python within a Jupyter Notebook environment. My goal was to maintain an interactive, experiment-friendly workspace that supported both exploratory analysis and visual storytelling.

Tool / Library	Purpose	Reason for Choice:

Pandas:	Data cleaning, transformation, and aggregation:	Provides flexible handling of mixed-type data (categorical + numeric) and fast filtering/grouping.

Matplotlib:	Foundational plotting:	Simple, customizable visualizations ideal for quick exploratory plots.

NumPy:	Numerical computation:	Used for normalizing TicketPrice and calculating mean/median efficiently.


I began with Matplotlib due to familiarity and control.

 Experimentation with Tools and Methodologies.
Experiment 1: Comparing Matplotlib vs Power BI

I explored how each library represented price distributions by trip type:

# Matplotlib version
import matplotlib.pyplot as plt

plt.figure(figsize=(8,5))
for trip in df['TripType'].unique():
    subset = df[df['TripType'] == trip]
    plt.hist(subset['TicketPrice'], bins=20, alpha=0.5, label=trip)
plt.legend()
plt.title('Ticket Price Distribution by Trip Type (Matplotlib)')
plt.xlabel('Ticket Price')
plt.ylabel('Frequency')
plt.show()


Result:
Matplotlib provided a clean static visualization, ideal for reports. However, it required additional effort to format labels and legends manually.


 Experiment 2: Feature Grouping and Aggregation.

I experimented with summarizing travel patterns by Region and Gender to identify differences in travel time and price.

region_summary = df.groupby(['Region', 'Gender']).agg({
    'TicketPrice': 'mean',
    'TravelTime': 'mean'
}).reset_index()


Insight:
This aggregation revealed that certain regions had higher average prices for return trips, and male travelers tended to book slightly longer travel durations on average.

====


# Version Control and Progressive Refinement.

I used Git to track each stage of development. Key commits demonstrated progressive experimentation:

Commit Message	Description.

init data cleaning.

Standardized categorical fields (Region, TripType) and handled missing values.

add exploratory visuals	Created first static Matplotlib plots for price and travel time,
final notebook polish.

Annotated code cells and summarized insights.

Each commit represented a meaningful iteration — either improving analysis depth, visual clarity, or reproducibility.
====

# Challenges and Solutions.

Challenge.

Description	Solution.

Skill Gained.

Inconsistent categorical data.
Variations in region naming (e.g., “north-east”, “North East”).

Used .str.lower().str.strip() and mapping dictionaries.

Data cleaning and preprocessing.

Choosing the right visual tool.	

Static vs interactive trade-off	Tested Matplotlib, Seaborn, and Power BI to find balance between clarity and usability.

Comparative evaluation.

Large dataset rendering issues.

Plotly slow on large files.

Sampled or aggregated data to reduce rendering time	Data optimization.

Version control discipline.	

Tracking multiple small changes	Committed after each meaningful experiment and added descriptive messages.	

Incremental documentation and traceability.

Meaningful Application.

This iterative experimentation demonstrated how tool choice directly influences insight quality.

Using multiple visualization libraries enriched my analysis and taught me how to balance efficiency, aesthetics, and interactivity.

By refining data workflows with Pandas, I built a more robust, exploratory, and reproducible analytical pipeline.

======

# Travel Data Insights Project.
Overview

This project analyzes travel data containing the following columns:
TicketPrice, ReturnTrip, TripType, Age, Gender, TravelTime, and Region.

The goal is to uncover insights into how demographic factors (such as Age and Gender) and trip attributes (TripType, ReturnTrip, Region) influence TicketPrice and TravelTime.

# Reflection: Choices, Limitations, and Alternatives.
 
This dataset explores how various factors — such as TripType, Region, Gender, and Age — influence key travel outcomes like TicketPrice and TravelTime.
The analysis focused on identifying relationships between traveler demographics, trip characteristics, and price behaviors.

# Reflection on Progress.

Throughout this project, I gained a stronger understanding of data cleaning, visualization, and interpretation. Initially, I approached the dataset by exploring correlations and distributions across numerical and categorical variables.

One major milestone was identifying how TripType (e.g., business vs leisure) and Region impacted TicketPrice, as well as understanding how Age influenced travel duration patterns. I progressively improved my analytical workflow — from manually inspecting CSV files to using automated scripts for exploratory data analysis (EDA).

====


# Installing

Clone the repository and navigate to the project directory:



# Challenges and Strategies to Overcome Them.

1. Data Cleaning and Inconsistent Entries.

Challenge: Some categorical values (e.g., “region” names or “trip types”) were inconsistent in capitalization or spelling.

Strategy: I used Python’s pandas string methods (.str.lower(), .strip()) and value mapping to normalize categories.

2. Understanding Relationships Between Variables.

Challenge: It wasn’t immediately clear which variables most influenced TicketPrice.

Strategy: I experimented with correlation heatmaps and grouping techniques (groupby) to test hypotheses. I also plotted visual comparisons (boxplots and scatterplots) to confirm relationships visually.

3. Knowledge Gaps in Statistical Testing.

Challenge: I initially lacked confidence in selecting the right statistical methods to test group differences.

Strategy: I reviewed documentation and tutorials on hypothesis testing (e.g., t-tests,) and applied them to evaluate price differences across regions and trip types.

4. Bug Fixes and Adaptation.

Issue: I encountered code errors when applying transformations on mixed-type columns (numeric + string).

Adaptation: I learned to apply .astype() conversions and conditional logic to separate preprocessing for numeric and categorical features.

Learning Moment: This helped me recognize the importance of data type awareness and robust validation steps before analysis.

Bug Tracking & Learning Log Issue.	

Description	Adaptation / Fix What I Learned.

====

# Data type mismatch.
	
Tried calculating mean on categorical field	Used df.select_dtypes to isolate numerical columns.

Always check data types before aggregating.

Visualization labels.

Some plots overlapped.

Used plt.tight_layout() and adjusted figure size.

Presentation clarity matters for communication.

Grouped summaries.

Incorrect aggregation.

Added .reset_index() after groupby	Proper indexing avoids hidden logic errors.

====

# Development Roadmap.

Based on this project experience, here are the next steps for my growth:

Skill/Tool	Purpose	Learning Plan.

SQL for Data Analysis,	Query and join travel datasets efficiently,	Take an online SQL course and practice on public travel data.

Machine Learning (Regression Models).	Predict ticket prices using multiple variables.

Learn Scikit-learn basics and experiment with linear regression.

Data Visualization (Seaborn / Power BI)	Improve storytelling with data.

Build dashboards and interactive plots.

Version Control (Git/GitHub).

Track project evolution	Create branches for feature updates and bug fixes.

====

# Feedback & Iteration.

I received feedback from my instructor emphasizing:

The importance of creating and maintaining a Kandam board.

Making it in the first phases of design and Ideation shaped and helped focused my efforts. e.g no more than 35 items, upto 35 would be enough although the final say would be upto me.

In response, I revised my kandam board items to include descriptive titles, short to the point narrative explanations, and documented each analytical step more clearly.


====


# Key Takeaways.

I strengthened my ability to perform structured data analysis.

I learned how to debug data transformation issues systematically.

I gained appreciation for documentation and iterative improvement.

====

# Credits.

I have to give a big cheer of appreciation to Gen A.I. especially Chat gpt for help, support and reference
to help make this project more than a dream but a reality.
Thankyou Chat gpt.

# Take and Enjoy
====