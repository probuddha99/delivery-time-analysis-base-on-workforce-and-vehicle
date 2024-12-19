# Delivery Performance Analysis Base On Workforce And Vehicle

### Project Overview 
This data analysis project aims to provide insight into the delivery performance of Amazon . By analyzing various aspect of delivery data , we seek to identify trends , make data-driven recommendations, and gain a deeper understanding of company’s performance .

### Data Source 
The primary data set used for this analysis is the “amazon_delivery.csv” file, containing detailed information about deliveries completed by the company .

### Tools
Excel : Data cleaning, Analysis , Dashboard 

### Data Cleaning/Prepration 

In the initial data prepration phase we performerd following tasks :
1. Data loading and inspection.
2. Created a distance column which measures distance between store and drop location. With  ```( =6371 * 2 * ASIN(SQRT(SIN(RADIANS(Drop_Latitude - Store_Latitude) / 2)^2 + COS(RADIANS(Store_Latitude)) * COS(RADIANS(Drop_Latitude)) * SIN(RADIANS(Drop_Longitude - Store_Longitude) / 2)^2)) )```
3. Created a speed of vehicle column.
4. Categorized Agent age , Agent Rating and distance .
5. Flitered out Outliers in distance .

### Expletory Data Analysis 
- How does agent rating influence delivery time across different age groups?
- How does delivery time vary across distance categories for each vehicle type?
- Which vehicle type has the highest average speed?

  ### Results/Findings
- Vehicle Speed and Delivery Efficiency:
  
1. Scooters have the highest average speed but may struggle with long-distance deliveries, as their delivery times increase substantially beyond 10 km.  
2. Vans, while not the fastest in speed, perform best for both short and long distances, indicating a more balanced trade-off between speed and efficiency.
3. Motorcycles are the slowest in terms of speed and delivery times, particularly over longer distances.
- Age Group Implications:
1. Younger groups (20–26) have faster deliveries across vehicles, likely benefiting more from higher-rated agents and faster vehicle types.
2. Older groups (35+) experience the longest delays, which could be attributed to less efficient vehicles (motorcycles) and lower agent ratings.
- Agent Ratings:
1. Higher agent ratings correlate with faster delivery times, particularly for Vans and Scooters.
2. Lower agent ratings significantly hinder delivery times, especially when coupled with slower vehicles (e.g., motorcycles) .


### Recommendation 
- Offer specialized training and tools for 35+ agents to improve their efficiency and reduce delivery times.
- Use Scooters for short distances, Vans for long distances, and limit Motorcycles to urban routes.
- Implement a smart system that allocates the most efficient vehicle type based on delivery conditions.





