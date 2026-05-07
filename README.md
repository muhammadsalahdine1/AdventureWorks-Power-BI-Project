# AdventureWorks Power BI Dashboard

This project is an end-to-end Power BI dashboard built on the **AdventureWorks** dataset. It provides interactive insights into sales performance, product demand, customer behavior, and shipping logistics. The dashboard is designed for business stakeholders to monitor key metrics and make data-driven decisions.

## 📊 Dashboard Features

### Key Performance Indicators (KPIs)
- **Total Orders**: 31K
- **Total Due**: $10.19M
- **Total Tax**: $123.22M
- **Total SubTotal**: $109.85M
- **Total Freight**: $3.18M
- **Average Delivery Days**: 12 days

### Interactive Visuals
- **Orders by Online Order Flag** (True / False)
- **Orders by Weekend** (Yes / No)
- **Orders by Product Name** (Top products like Water Bottle, AWC Logo Cap, Sport-100 Helmet, etc.)
- **Total Due by Group** (North America, South America, Africa)
- **BusinessEntityID Filter** (270, 280, 290 ranges)

### Filters & Slicers
- Measures
- Dim Customer
- Dim Date
- Dim Product
- Dim SalesPerson
- Dim ShipMethod
- Dim Territory
- Fact Sales

## 🛠️ DAX Measures Used

A robust set of DAX measures was created to support dynamic analysis:

| Measure Name | Formula Purpose |
|-------------|----------------|
| `#Orders` | Distinct count of SalesOrderID |
| `#Shipped` | Orders using ShipDate relationship |
| `#Delivered` | Orders using DueDate relationship |
| `AVG DeliveryDays` | Average delivery days per order |
| `Total Due` | Sum of TotalDue per order |
| `Total SubTotal` | Sum of SubTotal per order |
| `Total Freight` | Sum of Freight per order |
| `total Tax` | Sum of TaxAmt per order |
| `2012TotalDue` | Total Due for 2012 |
| `EuropeOnlineOrdersSimple` | Online orders in Europe |

### Dynamic Date Table
A calculated `Dim Date` table was generated using DAX to support time intelligence:
