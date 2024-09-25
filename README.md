# Airbnb Listings Analysis - Paris

This project involves analyzing Airbnb listings data with a focus on Paris. The data is processed and visualized to provide insights into neighborhood pricing, accommodations, and host trends over time.

## Dataset
The dataset used in this project is `Listings.csv`, which contains information about various Airbnb listings.

## Objectives
1. **Data Cleaning and Preparation**: 
    - Convert relevant columns to appropriate data types.
    - Filter the data to include only listings from Paris.

2. **Analysis**:
    - Group listings by neighborhood and calculate the average price.
    - Filter and analyze data for the most expensive neighborhood.
    - Examine host trends over time by calculating new hosts and average prices by year.

3. **Visualization**:
    - Create visualizations to highlight trends such as neighborhood pricing and new host growth over time.

## Key Steps
1. **Data Import**: The data is read using `pandas` with appropriate encoding to handle special characters.
    ```python
    listings = pd.read_csv('Listings.csv', encoding='latin1', low_memory=False)
    ```

2. **Filtering Data**: Focus on Paris listings and relevant columns.
    ```python
    paris_listings = listings[listings['city'] == 'Paris'][['host_since', 'neighbourhood', 'city', 'accommodates', 'price']]
    ```

3. **Grouping Data**: Group by neighborhood and calculate the average price.
    ```python
    paris_listings_neighbourhood = paris_listings.groupby('neighbourhood')['price'].mean().reset_index()
    ```

4. **Visualizations**:
    - Horizontal bar chart of average price by neighborhood.
    - Line charts showing new hosts and average price over time.
    - Dual-axis line chart displaying both trends together.

## Visualizations
- **Average Price by Neighborhood**: A horizontal bar chart that shows the average price of Airbnb listings in different Paris neighborhoods.
- **New Hosts Over Time**: A line chart representing the count of new Airbnb hosts over the years.
- **Average Price Over Time**: A line chart showing how the average price of listings has changed over time.

## Acknowledgements 
Maven Analytics

## Contact
For further inquiries, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/faiq-syed-7494b5197/).

## Requirements
- Python 3.x
- Pandas
- Seaborn
- Matplotlib

To install dependencies, use the following command:
```bash
pip install pandas seaborn matplotlib

## Contact
For further inquiries, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/faiq-syed-7494b5197/).
