# Sales Analytics Dashboard

![Alt txt](images/image.png)

## Business Understanding

The purpose of this project is to develop an interactive and insightful sales dashboard using Power BI. The dashboard aims to provide stakeholders with a comprehensive view of key sales metrics, trends, and performance indicators across various dimensions, such as time, territory, product line, and customer demographics.

### Objectives:

- To enable data-driven decision-making by visualizing critical sales data.
- To identify trends and highlight growth opportunities by analyzing sales distribution, customer purchasing patterns, and product performance.
- To support sales strategies by pinpointing high-performing territories and products, aiding in resource allocation and targeting efforts.

The `dashboard` will cater to:

1. Sales Teams - for monitoring targets and identifying high-potential customers and regions.
2. Marketing and Strategy Departments - to tailor marketing campaigns based on regional sales data and popular products.
3. Executive Management - for high-level insights into the organization’s sales performance.

## Data Understanding

The dataset includes three main files:

- Main Data: Records of individual sales transactions, capturing order details, product specifics, customer info, and branch locations.
- Product Master: Details about each product, allowing analysis by product line, category, or specifications.
- Data Dictionary: Definitions and descriptions of each field across the datasets.

### Key Columns in Main Data:

**Order Details**:

`OrderNumber, QuantityOrdered, PriceEach, OrderLineNumber, Sales, Status`

- These columns capture details of each transaction, including quantities, pricing, and total sales amounts.

**Temporal Information**:

`QTR_ID, DAY_ID, MONTH_ID, YEAR_ID`

- These columns were combined into a single Date column for easier time-based analysis.

**Product Information**:

`ProductCode`

- Used to link sales transactions to product details in the Product Master dataset.

**Customer Information**:

`CustomerName, Phone, AddressLine1, City, PostalCode, Country, ContactName`

- Captures details about each customer and their location.

**Branch Information**:

`Branch, Territory`

- Provides data on the branch responsible for each sale and the territory it serves.

The `Main Data` has 22 columns, with missing values in two fields:

* Postal Code: 76 missing values, filled with 0 as a placeholder for unknown postal codes.
* Territory: 1,074 missing values, filled based on country:
  - we assigned USA and Canada entries with missing Territory with "NA" (North America).

To provide additional product information in the analysis, we merged the Main Data with the Product Master dataset using an inner join on ProductCode. This enriched the dataset with product-specific details and created a comprehensive dataset `sales` for analysis and dashboarding.