# Power-BI-Data-Modeling-Transformation-Project_-Store_Data-

This Power BI project demonstrates data profiling, data cleaning, transformation, and star-schema modeling using an Excel dataset containing:

Dim Customer

Dim Product

Dim Promotion

Fact Table

🔍 Data Profiling & Cleaning
Dim Customer

Updated data types for consistency:

Customer ID → Text

Pincode, Phone Number → Whole Number

City, Customer Name, State, Email → Text

Enabled:

Column Distribution

Column Quality

Dim Promotion

Added Conditional Column → Percentage

Created 5 rules returning discount values (20%, 10%, 50%, 70%, etc.)

Fact Table

Corrected data types:

Date → Date

Customer ID & Promotion ID → Text

Units Sold → Whole Number

Original Price/Unit, Total Sales, Discount %, Discount Value were 100% null — later rebuilt.

🔄 Data Transformation

Merged Fact Table with Dim Promotion (Left Outer Join) to bring in Price per Unit

Added Total Sales = Units Sold × Price per Unit

Merged again to pull Discount Percentage

Added:

Discount Value = (Total Sales × Discount %) / 100

Net Sales = Total Sales – Discount Value

Rebuilt all calculated fields and removed outdated null columns

🏗️ Data Modeling

Added the missing Promotion table to Model View and built relationships:

Dimension Table	Key Column	Fact Relationship
Dim Product	Product ID	1 → Many (Fact Table)
Dim Promotion	Promotion ID	1 → Many (Fact Table)
Dim Customer	Customer ID	1 → Many (Fact Table)

Settings:

Cross filter direction: Single

Relationships: Active

Outcome: A clean, optimized Star Schema.

✅ Project Highlights

✔ Data profiling & quality checks
✔ Conditional columns and custom calculations
✔ Merge operations & discount logic
✔ Rebuilt sales/discount measures
✔ Proper data modeling with 1-to-many relationships
