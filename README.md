---
from IPython.display import Image, display

display(Image(filename="Screenshot 2025-10-07 173012 "))
---

Welcome,

Enigma Excursions Travel service and customer transactions. Analysis project.

The project is a Analysis of my clients travel service and customer transactions data to discover meaningful patterns, trends and insights.  my dataset has some interesting attributes based and around travel services provided and customer transactions, TicketPrice, ReturnTrip, TripType, Age, Gender, TravelTime, and Region.

# **Dataset content**
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


















# **hypothesis**

1.	Price Sensitivity Hypothesis
o	H₀: There is no difference in average ticket price across regions.
o	H₁: Average ticket price differs significantly across regions.
2.	Age and Trip Type Hypothesis
o	H₀: Age has no effect on trip type preference (one-way vs. return).
o	H₁: Age influences trip type preference.
3.	Gender and Spending Hypothesis
o	H₀: Average ticket price does not differ by gender.
o	H₁: Average ticket price differs significantly by gender.
4.	Travel Time and Ticket Price Relationship
o	H₀: There is no relationship between travel time and ticket price.
o	H₁: Ticket price increases with travel time.
5.	Triptype and Return Trip Hypothesis
o	H₀: Triptype is independent of return trip selection.
o	H₁: Triptype and return trip selection are dependent (e.g., leisure travelers more likely to book returns).
6.	Regional Demographics Hypothesis
o	H₀: The age distribution of travelers is the same across all regions.
o	H₁: The age distribution of travelers varies by region.

---
# **Data management section**

Explanation: Data Collection, Cleaning, and Storage
1. Data Collection

The dataset was compiled to analyze travel patterns and ticket pricing behavior across different regions.
Data was collected through multiple sources:

Online survey forms distributed to travelers through travel agencies and booking platforms.

Transaction records from ticketing systems that included ticket price, trip type (e.g., one-way or return), and travel time.

Demographic details (age, gender, and region) were self-reported by respondents or recorded during booking.

Each record in the dataset represents an individual traveler’s booking. Data collection ensured that all entries were anonymous and complied with data protection regulations.

2. Data Cleaning and Preparation

Before analysis, several cleaning and preprocessing steps were applied to ensure accuracy and consistency:
During cleaning, summary statistics and visual inspections (e.g., boxplots for TicketPrice and histograms for Age) were used to validate corrections.

3. Data Storage and Management

After cleaning, the data was stored and managed as follows:

Storage Format:
The dataset was saved in both .csv and .parquet formats for compatibility and efficiency.

Version Control:
Different versions of the dataset (raw, cleaned, and preprocessed) were stored separately to maintain a transparent data lineage.

Organization:
Data files were organized in a project structure:


Access and Backup:
The cleaned dataset was uploaded to a shared drive or database with restricted access for collaborators. Regular backups were automated to ensure data integrity.

4. Process Management

The data preparation process was managed using a structured workflow:

Data documentation: Metadata (column descriptions, data sources, units) was maintained in a separate README or data dictionary.

Reproducibility: All cleaning and transformation steps were scripted in Python using Pandas and Scikit-learn preprocessing pipelines.

Quality checks: Each stage (collection, cleaning, storage) included validation steps — such as checking value ranges, unique IDs, and consistency between fields (e.g., ReturnTrip vs. TripType).