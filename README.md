# thai-inspection
Goal: Clean and visualize a health inspection data set
1. Using the language and data store of your choice, create an ETL (Extract, Transform & Load) job to ingest this ~500k rows DOHMH New York City Restaurant Inspection Results data set from NYC Open Data

<UL>
<LI>Since SQL was my language of choice, I preformed an ELT job instead of an ETL. 
<LI>Using PostgreSQL, I imported the CSV using a COPY command.
<LI>The details for each violation were not pertinent to the task at hand as well as causing duplicate rows for each restaurant, so all repeating elements were grouped in a SQL query while leaving only the count of violation for each grade date.
</UL>

2. In addition to submitting working code for the ETL job, please include the schema design along with a quick explanation for the choices made.
<UL>
<LI>Since SQL was my language of choice, I preformed an ELT job instead of an ETL. 
<LI>Using PostgreSQL, I imported the CSV using a COPY command.
<LI>The details for each violation were not pertinent to the task at hand as well as causing duplicate rows for each restaurant, so all repeating elements were grouped in a SQL query while leaving only the count of violation for each grade date.
</UL>
