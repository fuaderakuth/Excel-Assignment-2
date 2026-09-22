# Excel-Assignment-2
## Data Cleaning and Transformation

The dataset analysis "Excel Assignment 2 - Data Cleaning and Transformation" started firstly with removing duplicates and moving to other data cleaning methods like, fixing inconsistent data using Power Query. Further steps done are listed below:

1. Handling Missing Values.
    *  Missing Price has been adjusted with identical products median as the total median of the 'Price' column doesn't match to the identical products prices and for "Camping Tent", the total median is taken after entering the other two missing values.
    *  Products with missing categories replaced with identical products categories and nature of product. For instance, product Backpack's blank category is replaced with Accessories matching to the Laptop Bag's category. 
      
2.  Correcting Inconsistent Data.
    * Data in the Products columns were with inconsistent text formats, transformed the entire column by formatting "Capitalize Each Word" built in function  in power query.
    * There were few typos in the category column such as "Electroni" instead of "Electronics". Fixed them with the "Find and Replace" function.    
      
3. Removing Duplicates.
    * The duplicates were removed upfront to keep the data integrity, this was again done through power query.
      
4.  Splitting and Merging Data.
    * The "Product ID" were split into two new columns, "Manufacturing Date" and "Country Code" using the Text to Column's fixed width feature and formatting the new field as "Date". While the "Manufacturing Date" field split successfully, the "Country Code" field came with error as "#NAME?", applied "RIGHT" function to split the country code. Upon further research, found the Manufacturing field could also retrieve the intended result with "LEFT" functions as " =DATEVALUE(LEFT(A2,6)". 
    * Merged the "Brand Name" and "Product Name" into new column named "Product Brand" using Ampersand function (=B2& " " &A2)

5. Number Formatting.
    * The data type for the "Price" column changed to currency format via the Home Ribbon's Number format section.
    * Manufacturing Date's format set to the "DD-MM-YYYY" format by default when the "Text to Column" feature's is used as the format "Date" was selected.
    
6. Conditional Formatting:
    * Price column is formatted with "Data Bar" instead of Color Scales, as the missing prices cell replaced with a value in the field were marked with yellow color.
    * A custom rule were created in "Category" field to highlight "Electronics" in green color. Steps as below" 
      Conditional Formatting > New Rule > Format only cells that contain > Specific text > Containing 
