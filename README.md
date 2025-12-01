# Group 2 MIST 4610 Project 2

## Team Members
- Yesha Ghandi
- Bradley Guy
- Ivan Jaiwant
- Yusuf Kshem
## Data Model
Our model is based on the operations of a digital music store that sells individual tracks and albums to customers. The core business process is captured through the Customer, Employee, Invoice, and Invoice_Line entities, which together represent who is buying music, who is supporting them, and what was purchased on each transaction. The Employee table stores staff information such as name, title, hire date, and contact details, and includes a self-referencing relationship that designates supervisors within the organization. Each Customer record contains personal and contact information, as well as a foreign key linking them to a support representative in the Employee table, reflecting the one-to-many relationship between employees and the customers they manage. 

The purchasing workflow is modeled through the Invoice and Invoice_Line tables. Each invoice represents a single customer transaction and includes attributes such as invoice date, billing address, and total amount. Because a single invoice can contain many purchased items, there is a one-to-many relationship between Invoice and Invoice_Line. The Invoice_Line table captures each line item on a bill, including the track purchased, quantity, and unit price. This design allows the store to track revenue at both the invoice level and the individual track level, supporting detailed sales and profitability analysis.

The music catalog itself is represented by a set of related entities centered on the Track table. Each track includes attributes such as name, composer, duration in milliseconds, file size in bytes, and unit price. Tracks belong to a specific Album, which in turn is associated with a single Artist, forming a one-to-many relationship from Artist to Album and from Album to Track. Additional descriptive attributes are modeled through the Genre and Media_Type tables: each track is linked to exactly one genre (e.g., Rock, Jazz, Classical) and one media type (e.g., MPEG audio file, AAC audio file), standardizing how content is categorized and stored.

Customer listening behavior and curated content are modeled through Playlist and Playlist_Track. A playlist is a named collection of tracks, and because a single track can appear on many playlists while each playlist can contain many tracks, these entities are connected via the associative Playlist_Track table in a many-to-many relationship. Overall, this schema provides a comprehensive and relational view of the music store’s operations—connecting employees, customers, invoices, and the full music catalog—enabling meaningful analysis of sales trends, customer preferences, and catalog performance.

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

1.  Query 1 lists the genre name, the total number of orders, the total number of tracks sold, the total revenue generated, and average revenue metrics (average order value and revenue per order) for each genre.

Query 1 helps analysts understand which music genres drive the most sales and revenue for the store. This information highlights the genres that are most popular, most profitable, and most frequently purchased, supporting decisions related to marketing, inventory expansion, licensing priorities, and customer targeting.

<img width="779" height="328" alt="query1" src="https://github.com/user-attachments/assets/3d62c248-ef46-4e55-b13c-faab318213cf" />

2.  Query 2 lists each customer’s name, total number of orders, average order value, and assigns two classifications: a customer value tier (high, medium, or low) and a purchase frequency category (frequent, regular, or occasional).

Query 2 helps analysts understand the purchasing habits and value level of each customer. By grouping customers into behavior-based segments, the business can identify its most profitable and loyal customers, target marketing efforts more effectively, and design retention strategies tailored to different customer groups. This segmentation supports stronger customer relationship management and more efficient decision-making.

<img width="911" height="427" alt="query2" src="https://github.com/user-attachments/assets/95da14db-0a23-4711-a346-423745036761" />

3.  Query 3 lists each country, the total number of customers, the total number of orders, the total revenue generated, and assigns a performance tier based on how each country’s revenue compares to the global average.

Query 3 helps analysts compare sales performance across countries and identify which international markets are top performers, average performers, or underperforming. This information supports strategic decisions such as targeting high-value regions, reallocating marketing resources, and recognizing countries with growth potential.

<img width="913" height="424" alt="query3" src="https://github.com/user-attachments/assets/9b4c66c4-b9bb-4e18-98bd-0a182d68f00b" />

4.  Query 4 lists each artist’s name, the total number of albums and tracks they have, the total revenue generated from their music, and assigns a demand category based on how many tracks were sold (very high, high, moderate, or low demand).

Query 4 helps analysts identify which artists are most popular and generate the highest demand among customers. This information can guide decisions related to promotions, featured playlists, licensing investments, and understanding which artists contribute most to overall store performance.

<img width="913" height="427" alt="query4" src="https://github.com/user-attachments/assets/a1971a10-d302-469c-9924-43d3d893452a" />

5.  Query 5 lists each employee’s name, job title, days employed, the total revenue generated from their assigned customers, and their average revenue per customer.

Query 5 helps identify which employees contribute the most to company revenue, allowing managers to evaluate performance, recognize top performers, and determine where additional training or support may be needed. This analysis supports workforce planning, sales strategy, and customer relationship management.

<img width="913" height="428" alt="query5" src="https://github.com/user-attachments/assets/efd94541-e4da-499a-98f1-556a877c16c4" />




## Visualizations

## Database Info
Name of the database: cs_yrk51993

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL Group2_Qx();

Where 'x' refers to the Query number.

