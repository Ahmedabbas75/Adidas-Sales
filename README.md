## 1- Dashboard :
</p>
  <p float="left">
  <img src='DashBoard\screen one.png'/>
  </p>
  <img src='DashBoard\screen two.png'/>
</p>

## 2- About the Dataset :
An Adidas sales dataset is a collection of data that includes information on the sales of Adidas products. This type of dataset may include details such as the number of units sold, the total sales revenue, the location of the sales, the type of product sold, and any other relevant information.

Adidas sales data can be useful for a variety of purposes, such as analyzing sales trends, identifying successful products or marketing campaigns, and developing strategies for future sales. It can also be used to compare Adidas sales to those of competitors, or to analyze the effectiveness of different marketing or sales channels.

There are a variety of sources that could potentially provide an Adidas sales dataset, including Adidas itself, market research firms, government agencies, or other organizations that track sales data. The specific data points included in an Adidas sales dataset may vary depending on the source and the purpose for which it is being used.

____________________________________________________________________________
## 3- Data Description :

- `Retailer` : Represents the business or individual that sells Adidas products directly to consumers.

- `Retailer ID` : A unique identifier assigned to each retailer in the dataset.

- `Invoice Date` : The date when a particular invoice or sales transaction took place.

- `Region` : Refers to a specific geographical area or district where the sales activity or retail operations occur.

- `State` : Represents a specific administrative division or territory within a country.

- `City` : Refers to an urban area or municipality where the sales activity or retail operations are conducted.

- `Product` : Represents the classification or grouping of Adidas products.

- `Price per Unit` : The cost or price associated with a single unit of a product.

- `Units Sold` : The quantity or number of units of a particular product sold during a specific sales transaction.

- `Total Sales` : The overall revenue generated from the sales transactions.

- `Operating Profit` : The profit earned by the retailer from its normal business operations.

- `Sales Method` : The approach or channel used by the retailer to sell its products or services.

_________________________________________________________________________________
## 4- In Mind Questions :

- ### General Questions related to the existence of
  - missing values?
  - wrong datatypes for columns?
  - complete duplicates in the data?
  - outliers in numerical columns?
 
- ### Business Questions
  -  What is the breakdown of sales by retailers, and how does it vary across different `retailers` ?
  -  What is total sales, Operating Profit in each `Region` ?
  -  What is total sales, Operating Profit in each `Product` ?
  -  What is total sales, Operating Profit in each `Season` ?
  -  What is total sales of each `year` ?
  -  What is total sales, Operating Profit in each `Sales Method` ?
  -  Does the Sales Method increase or decrease `during seasons` ?
  -  What is the distribution of sales by top 20 `state` ?
  -  What is the average price of `products per unit` ?

______________________________________________________________________________________
## 5- Conclusion :
  - `West Gear` and `Foot locker` emerge as the top retailers, capturing 27% and 24% of sales, respectively.
  - `West` and `Northeast` emerge as the top Region, capture 30% and 21% of sales respectively.
  - Top product categories such as `Men’s Street Footwear`, `Women’s Apparel`, and `Men’s Athletic Footwear`, which for 60% of total sales.
  - Sales increase in the `summer` and `winter` seasons, which represent 29 % and 24% of sales respectively.It may be due to school season or recreational breaks on the beach.
  - In `2021`, sales were much higher than in `2020`, and the main reason for this was Covid-19.
  - The `online` sales method ranked first with a percentage 37%, followed by `Outlet` Sales method with a percentage 33%.
  - The sale of products `decreases` significantly in `Autumn` and `Spring`.
  - `New York` and `California` It has the highest sales.
  - `Women's Apparel` and `Men's Apparel` it is the most expensive product.
______________________________________________________________________________________
## 6- 💡Summary :
  - #### Drop rows have missing value in `Price per units` columns, Because This values are somewhat very small.
  - #### In `Invoice Date column` i extract some values such as `year`, `month`,`day` and create `season` column based on month column and i drop it.
  - #### In `Product`, There were duplicate values due to a spelling error and fixed this.
  - #### In `Price per Unit`, i remove Dollar Sign and convert data type to numeric.
  - #### In ` Units Sold`, replace comma with empty string and  convert data type to integer.
      - ⚠️ During discover this column I found zero values `Sales may have been returned by customer and money was refunded to him `
      - 💡 `I decided to drop them`
      
  - #### In `Total Sales` replace comma with empty string and convert data type to numeric.
      - ⚠️ During discover this column some values in "Total Sales" is incorrect  And so it some value in "Operating Profit" column in same row is incorrect
      - 💡 I fixed this by using some `calculations and adding some columns to help me fix this`.
  - #### In `Total Sales` i remove Dollar Sign,replace comma with empty string and convert data type to numeric.
