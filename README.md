# ITI
Contact : +212649931406 | mzq305@gmail.com
Shiny for International Trade Intelligence Dashboard
GitHub Repository Description for Shiny App
International Trade Intelligence Dashboard

This repository contains a Shiny application built in R for visualizing and analyzing international trade data. 
The dashboard provides an interactive interface to explore trade values and growth rates for exports and imports, with a focus on specific commodities identified by their HS (Harmonized System) codes. 
It features a clean and user-friendly design, making it easy to search for products, view trade trends over time, and analyze growth metrics.

Key Features:
Interactive Dashboard: Built using R Shiny, allowing users to select between exports and imports and search for products by HS code or description.
Trade Data Visualization: Displays trade values (in USD) as bar charts and growth rates (in %) as a smoothed line chart, with a legend positioned below the chart for clarity.
Growth Metrics: Includes annual growth rates and Compound Annual Growth Rate (CAGR) for the period 2017–2024, presented in a sidebar for easy access.
Formatted Outputs: Trade values are formatted with thousand separators (e.g., 1 000 000) for readability, and the main table labels trade values as "Value$".
Custom Styling: Features a professional design with the "flatly" Bootstrap theme and a custom title in Condensed Roboto font.
Data Source:
The app uses trade data from a local Excel file (US_MA.xlsx), which contains trade values in USD for various commodities, categorized by HS codes (6-digit level).
Commodity descriptions are fetched using the comtradr package, which interfaces with the UN Comtrade API.
Libraries Used:
shiny: For building the interactive web application.
plotly: For creating interactive charts with bars and smoothed lines.
DT: For rendering data tables.
comtradr: For accessing HS code descriptions via the UN Comtrade API.
tidyverse (including dplyr, tidyr): For data manipulation and processing.
readxl and rio: For reading the Excel data file.
bslib: For applying the "flatly" Bootstrap theme.
Setup Instructions:
Install R and RStudio: Ensure you have R (version 4.0 or higher) and RStudio installed.
install.packages(c("shiny", "plotly", "DT", "comtradr", "tidyverse", "readxl", "rio", "bslib"))
Set Up the Comtrade API Key:
The app uses the comtradr package to fetch HS code descriptions. Replace the API key in the code with your own:
You can obtain a free API key by registering at the UN Comtrade API portal.
Prepare the Data:
Place your trade data file (US_MA.xlsx) in the specified path (C:/Users/pc/Desktop/US_MA.xlsx), or update the file path in the code to match your local setup.
Run the App:
Open the script in RStudio and run it. The Shiny app will launch in your default web browser.
Alternatively, use shiny::runApp() in the R console from the project directory.
Usage:
Select a flow category ("Exports" or "Imports") from the dropdown.
Search for a product by its HS code (e.g., "010511") or description.
Click the "Search" button to display:
A table of trade values (in USD) for each year (2017–2024).
A chart showing trade values (bars) and growth rates (smoothed line).
Growth metrics (annual growth rates and CAGR) in the sidebar.
File Structure:
app.R: The main Shiny app script containing both the UI and server logic.
(Optional) US_MA.xlsx: The trade data file (not included in the repository; users must provide their own data).
Notes:
The app assumes the data file (US_MA.xlsx) has columns for flowcategory, Year, cmdcode_6, and value_usd. Adjust the data processing steps if your data structure differs.
The Condensed Roboto font is loaded via Google Fonts, requiring an internet connection. For offline use, host the font locally and update the CSS accordingly.
The app is designed for a specific dataset but can be adapted for other trade data with similar structures.
License:
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing:
Contributions are welcome! Feel free to open issues or submit pull requests for bug fixes, feature enhancements, or improvements.

