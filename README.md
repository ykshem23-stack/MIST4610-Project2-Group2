# Group 2 MIST 4610 Project 2

## Team Members
- Yesha Ghandi
- Bradley Guy
- Ivan Jaiwant
- Yusuf Kshem
## Data Model
Our model is based on the structure of global regions and the countries that belong to them. The Region entity represents large geographic areas across the world, containing attributes such as regionID, regionName, areaSqKm, climateZone, and description. Each region contains many countries, which is why there is a one-to-many relationship between the Region and Country entities.

For this project, we used the Chinook Music Store database and made the data model based on it. The database connects customers, invoices, tracks, albums, artists, genres, etc in order to analyze the sales performance from mutlpel different angles. With the help of the model, we were able to create queries that allows us to see business metrics such as, total revenue by genre, purchase frequency, and employee revenue .The visualizations also bring up key insights such as revenue being concentrated in a few top performing countries, most customers are occasional buyers with only a small segemt of them purchasing frequently, and  that  some of the artists genrate a disproportionate share of revenue. Both the model and the visualizations shows that the Chinook Music Store relies on a strong market, high demand artists, and a small loyal customer base. Due to this there can be opportunities to grow the mid tier counties while stringhteing the retention programs, and promoting top and emerging artists to diversify in order to increase the overall revenue. 

![IMAGE](https://github.com/user-attachments/assets/04755b08-36f2-4f99-82b5-ec9a010370d9)

## Data Dictionary
<img width="524" height="82" alt="artist" src="https://github.com/user-attachments/assets/dec91870-9fa9-4ce4-ad28-77b8599b46e1" />



<img width="524" height="101" alt="album" src="https://github.com/user-attachments/assets/4a4ab13d-8812-41fc-9453-d12b02e0a034" />



<img width="525" height="342" alt="employee" src="https://github.com/user-attachments/assets/67515b77-de4b-46ac-b270-83aa6aec003b" />



<img width="525" height="322" alt="customer" src="https://github.com/user-attachments/assets/03ef0d99-a427-4be4-950d-81506cfe68d1" />



<img width="524" height="81" alt="genre" src="https://github.com/user-attachments/assets/2fea49e1-0eb0-4b02-8eae-aeece1b698aa" />



<img width="526" height="82" alt="mediatype" src="https://github.com/user-attachments/assets/8e4e2142-48fe-40b5-aa67-c2acf84e6f15" />



<img width="527" height="220" alt="track" src="https://github.com/user-attachments/assets/055adaa3-d598-438a-85bb-91aca0318d96" />



<img width="526" height="221" alt="invoice" src="https://github.com/user-attachments/assets/d1937d27-97fb-43dd-aeab-1968999a871b" />



<img width="526" height="140" alt="Invoiceline" src="https://github.com/user-attachments/assets/dca6bd77-140b-4d08-b575-57eb60dbcce1" />



<img width="525" height="83" alt="playlist" src="https://github.com/user-attachments/assets/36e5f079-0c65-4f1d-a386-19282fe0cbd2" />



<img width="525" height="80" alt="playlisttrack" src="https://github.com/user-attachments/assets/c9a61288-af2f-4593-b4dd-e3d4c3062da4" />


## Queries
<img width="1056" height="438" alt="querycheck" src="https://github.com/user-attachments/assets/a4ed96b2-f3f0-4d50-bdf8-7b8adeb9cae3" />

1.  Query 1 lists the region name, the inflation category (High or Low), the number of countries in each category, and CPI statistics.

Query 1 helps analysts see which regions are experiencing high or low inflation relative to the global average. This information could guide economic policy decisions or investment strategies, highlighting regions where inflation is most severe or stable.

<img width="779" height="328" alt="query1" src="https://github.com/user-attachments/assets/3d62c248-ef46-4e55-b13c-faab318213cf" />

2.  Query 2 lists the region name, education tier (Low, Mixed, High), the number of countries in each tier, average minimum wage, and average primary and tertiary enrollment. 

Query 2 provides insight into the relationship between educational investment and economic outcomes by region. By identifying whether higher education levels correlate with higher wages, policymakers or international organizations can better target initiatives to improve economic performance.

<img width="911" height="427" alt="query2" src="https://github.com/user-attachments/assets/95da14db-0a23-4711-a346-423745036761" />

3.  Query 3 lists each country, its GDP, carbon emissions, and GDP per ton of carbon emitted. 

Query 3 evaluates economic efficiency in relation to environmental impact. This analysis could inform sustainability programs or investment in green technologies by showing which countries produce higher GDP per unit of pollution.

<img width="913" height="424" alt="query3" src="https://github.com/user-attachments/assets/9b4c66c4-b9bb-4e18-98bd-0a182d68f00b" />

4.  Query 4 lists each country, its GDP, GDP per tax percentage, and a tax category (High or Low). 

Query 4 examines whether higher taxes suppress economic growth. This could influence fiscal policy decisions or corporate investment strategies by highlighting countries where tax burden corresponds with economic performance.

<img width="913" height="427" alt="query4" src="https://github.com/user-attachments/assets/a1971a10-d302-469c-9924-43d3d893452a" />

5.  Query 5 lists each country, its population, GDP, and GDP per capita. 

Query 5 measures economic output per person, helping analysts compare living standards or evaluate economic efficiency. These insights can support development planning or global market assessments.

<img width="913" height="428" alt="query5" src="https://github.com/user-attachments/assets/efd94541-e4da-499a-98f1-556a877c16c4" />




## Visualizations

## Database Info
Name of the database: cs_yrk51993

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL Group2_Qx();

Where 'x' refers to the Query number.

