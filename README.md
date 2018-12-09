# thai-inspection
Goal: Clean and visualize a health inspection data set
1. Using the language and data store of your choice, create an ETL (Extract, Transform & Load) job to ingest this ~500k rows DOHMH New York City Restaurant Inspection Results data set from NYC Open Data

<UL>
<LI>Since SQL was my language of choice, I preformed an ELT job rather than an ETL. 
<LI>Using PostgreSQL as my data store, I imported the CSV using a COPY command.
<LI>The details for each violation were not pertinent to the task at hand and were causing duplicate rows for each restaurant, so all repeating elements were grouped in a SQL query while leaving only the count of violation for each grade date.
</UL>

2. In addition to submitting working code for the ETL job, please include the schema design along with a quick explanation for the choices made.
<UL>
<LI>My schema design consists of a new base table and a column list. 
<LI>I created my column list to preserve all columns in the original CSV.
<LI>The data types of variable character, integer, and date were assigned to the columns based off their format. The exceptions I ran into were building, zipcode, and phone, which would normally have a data type of integer, but were set to variable character to provide for a smooth load that accounted for entries such as "N/A."
</UL>
