# Group 2 MIST 4610 Project 2

## Team Members
- Yesha Gandhi
- Haley Catudal
- Ivan Jaiwant
- Yusuf Kshem
## Data Model
Our model is based on the operations of a digital music store, "Chinook Music Store", that sells individual tracks and albums to customers. The core business process is captured through the Customer, Employee, Invoice, and Invoice_Line entities, which together represent who is buying music, who is supporting them, and what was purchased on each transaction. The Employee table stores staff information such as name, title, hire date, and contact details, and includes a self-referencing relationship that designates supervisors within the organization. Each Customer record contains personal and contact information, as well as a foreign key linking them to a support representative in the Employee table, reflecting the one-to-many relationship between employees and the customers they manage. 

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

4.  Query 4 lists each artist’s name, the number of albums they have released, the total number of tracks they produced, the total revenue generated from their music, and assigns a demand label based on the number of tracks sold (very high, high, moderate, or low demand).

Query 4 helps identify which artists are most popular and generate the most listener demand, allowing the business to understand which artists drive revenue and should be prioritized in marketing, playlist placement, inventory expansion, or promotional campaigns.

<img width="1552" height="800" alt="query4" src="https://github.com/user-attachments/assets/440dd3ca-d17d-4455-ad27-054af5fe4154" />

5.  Query 5 lists each employee’s full name, job title, the number of days they have been employed, the total revenue generated from the customers they support, and their revenue per customer.

Query 5 provides insight into employee performance by showing which support agents contribute the most to sales through their managed customers, helping management make informed decisions about employee development, workload balancing, recognition, and resource allocation.

<img width="1563" height="319" alt="query5" src="https://github.com/user-attachments/assets/055aa66b-8852-4ea8-ac97-255811ff458e" />




## Visualizations
<img width="3300" height="2600" alt="Chinook Music Store Analytics Dashboard-1" src="https://github.com/user-attachments/assets/6523f4be-d192-4aec-add5-7fde80065e60" />

### Country Performance by Revenue
* This bar chart displays the total revenue generated by each country and categorizes them into performance tiers based on how their revenue compares to the global average. This visualization helps identify high-performing markets (Tier 1 and Tier 2), as well as countries with lower revenue contribution (Tier 3 and Tier 4). Understanding these geographic patterns is valuable for targeting marketing efforts, prioritizing resource allocation, and recognizing regions with growth potential.

### Top 5 Artists by Revenue
* This chart highlights the top five artists who generated the highest total revenue from track sales. The visualization makes it easy to compare artist performance and understand which artists contribute most to store revenue. This information is beneficial for making decisions on featured content, promotional strategies, playlist placement, and inventory prioritization for popular artists.

### Number of Customers per Purchase Frequency
* This bar chart summarizes how many customers fall into each purchasing category: frequent buyers, regular buyers, and occasional buyers. The visualization provides clear insight into customer behavior and engagement levels. Understanding the distribution of customer purchasing habits helps the business tailor loyalty programs, personalize marketing, and identify opportunities to increase customer retention and repeat purchases.

## Database Info
Name of the database: cs_yrk51993

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL Group2_Qx();

Where 'x' refers to the Query number.

