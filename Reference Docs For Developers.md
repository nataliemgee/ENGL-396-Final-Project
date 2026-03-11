**FAQs for Developers**   
**What applications power the app?**  
The app is built using: 

- R  
- RStudio  
- Shiny   
- dplyr   
- ggplot2

**What version of R should I use?**   
R version 4.0 or above is recommended.

**What happens if I see “package not found” errors in the console?**   
Install missing packages in the Console: 

**Why does my app fail on deployment?**   
Common causes: 

- Missing R packages.   
- Incorrect file paths.  
- Incorrect working directory.   
- Case-sensitive file names.   
- Files outside of the MyFavoriteAlbums folder.   
- Incorrect CSV or data formatting.   
- Large files or memory issues. 

**Are column names case-sensitive?**   
Yes. Capitalization must match exactly. 

**Why do I need to restart the app after editing the CSV?**  
Shiny reads the data only when the app launches. It does not automatically refresh datasets while running.

**Does the app support APIs or databases?**   
No. The current architecture of the software can only accommodate local CSV file input. 

**Data & Validation Guide for Developers**   
This document will define the CSV structure for the My Favorite Albums dataset.

**Required File Location** 

- CSV file must be stored in the **data** folder  
- File name can be anything, but must end in `.csv` and follow the pathway:  
   `"data/_____.csv"`  
- Case-sensitive when deployed to the web

**Dataset Column Requirements and Input Rules (Case-Sensitive)**

| Column | Data Type  | Are Fields Required? | Field Input Rules  |
| :---- | :---- | :---- | :---- |
| Year | Numeric | Yes | Numeric (4-digit) |
| Ranking  | Numeric | Yes | Must be a positive integer. Ideally unique within each year. |
| Album | Text | Yes | Cannot be left blank. Consistent capitalization and spelling recommended.  |
| Artist | Text | Yes | Cannot be left blank. Consistent capitalization and spelling recommended.  |
| Rating  | Numeric (1-10) | Yes | Numeric only. Must be between 1-10. Decimals are allowed  |
| Vinyl | Mark with lowercase “v” | No | Blank OR “v”  |
| EP | Mark with all caps “EP” | No | Blank OR “EP”  |
| Live | Mark as “Live” | No | Blank OR “Live”  |

**Validation Requirements**   
Before running the application: 

- Column names match exactly   
- Required fields not empty   
- Year, Ranking, Rating are numeric entries   
- Ratings within 1-10  
- No unintended duplicates   
- App restarted after changes 

**Glossary for Developers**   
This glossary will define technical terms used in the development and deployment of the My Favorite Albums software.  
**R**  
An open-source programming language used for data analysis, computing, and visualization. R is the programming language used for the development of My Favorite Albums. 

**RStudio**  
An Integrated Development Environment (IDE) for R. It provides a workspace for developers to write code and run applications. RStudio is used to build, test, and launch the My Favorite Albums app.

**shinyapps.io**  
A cloud hosting platform that allows developers to publish Shiny applications online. This website enables the My Favorite Albums application to be accessed through a public web link without requiring users to install R or RStudio.

**app.R**  
The main application file that sources both the UI and operational server docs. This file is required to launch the Shiny application. 

**Case Sensitivity**   
The requirement that file names, column names, and object names must match capitalization exactly.   
Example: “albums.csv” is **NOT** the same as “Albums.csv”

**Console**   
The RStudio pane where commands are executed and error messages appear. 

**CSV (Comma-Separated Values)**  
A structured text file the application depends on as its sole source of data. 

- Each row \= one album  
- Each column \= one variable 


**Deployment**   
The process of publishing the My Favorite Albums software online so others can access the application via a URL.

**Shiny**   
An R package that allows developers to build interactive web applications directly from R code.