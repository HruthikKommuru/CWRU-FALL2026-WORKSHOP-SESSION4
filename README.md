# TrailMix Outdoors: Q3 Sales Reporting Brief

TrailMix Outdoors is a mid-size outdoor-gear e-commerce retailer serving individual shoppers and business customers across the West, Central, and East regions. Its assortment includes Footwear, Apparel, Camping Gear, Hydration, and Accessories. Leadership needs a reliable view of Q3 revenue to understand regional performance and the contribution of each product category.

You are a new analyst on the commercial analytics team. Your assignment is to **produce a clean, consolidated Q3 sales dataset, plus a short written summary of revenue by region and category, and a list of the data-quality issues you found and how you handled each one**.

The reporting period is July 1 through September 30, 2026. All monetary values represent US dollars (USD). The files are synthetic training extracts sized for a single class session; names and transactions are fictional.

## Provided data

Three regional sales exports are provided and must be merged into a consolidated dataset:

- `data/west_region_sales.csv`
- `data/central_region_sales.csv`
- `data/east_region_sales.csv`

`data/customers.csv` is the customer reference file. Use it to relate sales activity to customer records through the customer identifier.

## Data dictionary

Each sales row represents an exported order record for one product category. Quantity is the number of units recorded for that order; unit price is the price per unit, and sales amount is the recorded merchandise revenue. Sales amounts exclude shipping and sales tax.

The table below describes every column in each regional export. Read the column under the corresponding filename to identify its header.

| West export | Central export | East export | Meaning |
| --- | --- | --- | --- |
| `OrderID` | `order_id` | `order_id` | Business identifier for the order. |
| `OrderDate` | `order_date` | `order_date` | Recorded transaction date; determines the reporting period. |
| `CustomerID` | `customer_id` | `customer_id` | Customer identifier used to relate the order to the customer reference file. |
| `customer_segment` | `customer_segment` | `customer_segment` | Customer classification recorded in the sales export: Retail, Wholesale, or Outlet. |
| `Region` | `region` | `region` | Sales region associated with the order: West, Central, or East. |
| `product_category` | `product_category` | `product_category` | Merchandise category associated with the order. |
| `Quantity` | `quantity` | `quantity` | Recorded number of units. |
| `UnitPrice` | `unit_price` | `unit_price` | Recorded price per unit in USD. |
| `SalesAmount` | `sales_amount` | `sales_amount` | Recorded merchandise revenue for the order in USD. |

### Customer reference: `data/customers.csv`

| Column | Meaning |
| --- | --- |
| `customer_id` | Business identifier for the customer. |
| `name` | Customer name for the account. |
| `segment` | Customer reference classification: Retail (individual shoppers), Wholesale (business buyers), or Outlet (customers purchasing through the outlet channel). |
| `signup_date` | Date the customer account was opened. |

## Deliverables

Prepare a consolidated Q3 sales dataset that supports your report, a short written revenue summary by region and product category, and an issue log explaining your decisions. State any assumptions that affect the reported figures and make your work reproducible so another analyst can follow your process.

The repository contains the source inputs and this brief. Keep the original exports available as the record of what you received.
