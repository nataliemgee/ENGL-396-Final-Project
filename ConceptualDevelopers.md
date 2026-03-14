# **Conceptual Overview For Developers**   
## **About**   
My Favorite Albums is a web-based data analysis software that allows users to analyze, compare, and explore music albums across multiple years. The platform allows users to update displayed data and offers interactive visualizations and filters and gives users the ability to examine trends over time to evaluate individual artists, and assess highly rated albums. 

## **Key Features**  
My Favorite Albums is a web-based data analysis platform that provides seven tabs with different modes of data interpretation for users.  
### **The Seven Tabs Include:** 

- **Home:** This tab provides a comprehensive overview of the dataset and shows the total number of albums, total artists, and the artist with the most albums in the database.  
- **Number One Albums:** This tab displays the top-ranked album for each year in a selected  time range.  
- **Top Albums by Year:** This tab lets users select a year from a dropdown menu and lists all albums for the chosen year, ranked by rating.  
- **Artists’Albums:** This tab allows users to select an artist from an alphabetical dropdown menu and view all albums for the selected artist, with release year, rating, and average rating.  
- **Favorite Artists:** This tab lists top artists by average album rating, with options to filter by minimum albums and exclude EPs or live albums.  
- **Artist Comparison:** This tab allows users to compare two artists’ album ratings over time using a line chart.  
- **Vinyl:** This tab shows highly rated albums that the user does not own on vinyl, using a dropdown menu. 

## **Key Terms:** 

- **Dataset:** A structured CSV file that contains album information used by the application for all analysis and visualization.  
- **CSV File:** CSV or (Comma-Separated Values) is a file format that is used to store, in this case, album data, where each row represents an album and each column represents an attribute.   
- **R:** An open-source programming language and environment used mainly for statistical computing, data analysis, and data visualization.   
- **RStudio:** An integrated development environment (IDE) for R that provides a user-friendly interface and tools for writing, running, and debugging R code.   
- **Shiny:** Shiny is an R package that allows users to create interactive web applications that connect user inputs to updated outputs.   
-**shinyapps.io:** shinyapps.io is a cloud-based platform by RStudio that lets users deploy and share interactive R Shiny web applications.
- **UI (User Interface):** The front-end layout of the program including tabs, inputs, and output placeholders. 


## **Software & Data Requirements**   
My Favorite Albums was developed using R. The following items are needed to set up and launch the platform for developers:   
### **Software Requirements:** 

- R programming language (Version 4.0+ recommended)  
- RStudio  
- R packages  
  - shiny: to run the interactive web application   
  - dplyr: for data manipulation   
  - ggplot2: for plotting comparison charts 

### **File Structure:**   
All files are stored in this Git repository: [https://github.com/UW-Example-Student/MyFavoriteAlbums?tab=readme-ov-file](https://github.com/UW-Example-Student/MyFavoriteAlbums?tab=readme-ov-file)

### **Data Requirements:** 

- The program requires a CSV file. The filename and data can be customized, but it must include the following columns:   
- Columns: Year, Ranking, Album, Artist, Rating, Vinyl, EP, Live  
- Ensure correct data types for numerical and categorical fields  
- Use the included CSV file (data/album-rankings.csv) in the repository as a reference for formatting your own data.

## **Data Flow** 

- CSV Data Input: Album data is read from a CSV file using R, with numeric and categorical columns automatically typed.
- Data Cleaning & Preparation: Using dplyr, data is filtered, sorted, and transformed (e.g., calculating average ratings, excluding EPs/live albums) based on user selections.
- Connect to the UI: Shiny reacts to what the user selects in the app (like a year or artist) and updates the data for that tab.
- Show Results: The processed data appears as tables, charts, or text in the app. It updates automatically when the user changes their selection.
- Interactive Loop: User makes a choice, app updates data, results show instantly.

Album data is loaded from a CSV file and processed by R functions for each tab. The processed data is then sent to the Shiny UI, where it is displayed as tables, charts, or text based on what the user selects.


## **Limitations for Developers:** 

- This program is designed to work with CSV-formatted data and does not support external APIs. The programmed Shiny framework is optimized for a single-user, so scaling for multiple users at the same time may require additional modifications, not included in this documentation. Developers should ensure that shiny, dplyr, and ggplot2 are installed and up to date. 