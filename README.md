# thai-inspection
Goal: Clean and visualize a health inspection data set

<strong>1. Using the language and data store of your choice, create an ETL (Extract, Transform & Load) job to ingest this ~500k rows DOHMH New York City Restaurant Inspection Results data set from NYC Open Data</strong>

<UL>
<LI>Since SQL was my language of choice, I performed an ELT job rather than an ETL. 
<LI>Using PostgreSQL as my data store, I imported the CSV using a <a href="hpaxton2/thai-inspection/blob/master/load">COPY command</a>.
<LI>The details for each violation were not pertinent to the task at hand and were causing duplicate rows for each restaurant, so all repeating elements were grouped in a SQL query while leaving only the count of violation for each grade date.
</UL>

<strong>2. In addition to submitting working code for the ETL job, please include the schema design along with a quick explanation for the choices made.</strong>

<UL>
<LI>My schema design consists of a new base table and a column list. 
<LI>I created my column list to preserve all columns in the original CSV.
<LI>The data types of variable character, integer, and date were assigned to the columns based off their format. The exceptions I ran into were building, zipcode, and phone, which would normally have a data type of integer, but were set to variable character to provide for a smooth load that accounted for entries such as "N/A."
</UL>

<strong>3. Using your data store, generate a list of the top 10 Thai restaurants that meet your friend's criteria. You could simply provide a SQL query to answer this and export it into a data viz tool, but it be amazing if you could build a web frontend to answer the question.</strong>

<UL>
<LI>I created a SQL query that both transformed the data into the group as I described in step one and also created a list of restaurants that matched the given criteria.
<LI>There are far more than 10 Thai restaurants that receive A or B ratings, so I chose to narrow the search by grade date and the column I created that totaled the violations. To achieve a top 10, I only considered 2018 grades with the lowest number of total violations. 
<LI>The PostgreSQL table was connected to a Tableau Public account to be appropriately visualized and exported to the web. 
</UL>
  
<strong>4. Create a data viz or two showing the results of the question.</strong>
  
<UL>
<LI>I created a map that geocoded the location of the top 10 thai restaurants by using the Google Maps API through Tableau. I also formatted phone numbers by borough in the case of wanting to make a reservation and made a bar chart so my friend can view the cleanest possible option within the top 10 restaurants. 
<LI>I also created a table without the limit of 10 applied so my friend could view all Thai restaurants that meet their expectations by borough in the case they have exhausted their top 10 and still want an index of their options. 
<LI>Working Tableau visualization: https://public.tableau.com/views/thai_viz_0/Top10ThaiRestaurants?:embed=y&:display_count=yes&publish=yes. 
</UL>
   
