# **FAQs for General Users**   
### **What is My Favorite Albums?**  
My Favorite Albums is an interactive web application built using R, RStudio, and Shiny. This website allows you to explore, compare, and analyze album data through interactive tabs and visualizations. 

### **Do I need programming knowledge to use the website?**  
No. The website is designed for users with no programming experience. All website interactions occur through dropdown menus, sliders, and checkboxes. 

### **How do I move between tabs?**   
Use the navigation bar. Each tab name (Home, Number One Albums, Top Albums by Year, etc.) is clickable. 

### **Why didn’t my results update?** 

- Make sure to click Submit (if the tab includes one).  
- Try refreshing your browser.   
- If the issue persists, reload the page. 

### **What does “Exclude EPs and Live Albums” mean?**   
When checked, the app removes:

- EP (Extended Play) releases   
- Live albums 

from average rating calculations 

### **What does the vinyl filter do?**  
The Vinyl tab shows highly rated albums that are not marked with a lowercase “v” in the dataset, meaning they are not owned on vinyl. 

### **Can I add or edit album data directly in the app?**  
No. The application does not allow users to modify data. All album data comes from a pre-downloaded CSV file. If you want to create and implement your own CSV file, reference the developer tutorial on how to create a custom CSV file. 

### **Why are ratings fixed?**   
Ratings are based on the provided dataset. The application performs data analysis only, it does not adjust ratings dynamically.





# **Glossary for General Users**   
This glossary explains common terms that are used throughout the My Favorite Albums website. Definitions are written for users with little to no technical knowledge.

#### **Album**  
A collection of songs released by an artist or band. Albums are the main focus of this application. 

#### **Album Rating**   
A numerical score from 1 to 10 assigned to an album. 

- 10 \= the highest possible rating   
- 1 \= the lowest possible rating 

Ratings are fixed and come directly from the dataset used by the program.

#### **Artist**  
A musician, band, or musical group that creates and releases albums. 

#### **Artist Comparison**  
A feature in the application that allows you to select two artists and view a visual graph that compares their album ratings over a fixed period of time. 

#### **Average Rating**   
The average of all album ratings for a selected artist. The average is calculated by adding all album ratings and dividing by the total number of albums. 

#### **CSV File**   
A type of file used to store structures data in rows and columns. Each row represents an album, and each column represents information such as year, rating, or artist. 

#### **EP (Extended Play)**  
A shorter music release that contains more songs than a single and fewer than a full length album. EPs can be included or excluded from certain calculations. 

#### **Live Album**   
An album recorded during a live performance 

#### **Home Tab**   
The main landing page of the application.   
It displays: 

- Total number of albums   
- Total number of artists   
- Artists with the most albums in the database

#### **Ranking**   
The position of an album compared to others released in the same year. 

- A ranking of 1 means it is the top-ranked album for that year.   
- Lower numbers represent higher placement 

#### **Slider**   
A horizontal bar that allows you to select a range of values by dragging markers. Used in   
Number One Albums tab to choose a range of year. 

![Slider](Slider.png)

