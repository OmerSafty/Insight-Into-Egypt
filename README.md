# Insight-Into-Egypt
 Looking at different statistics throughout Egypt's history
## Introduction 
![Dashboardshowcase](https://github.com/user-attachments/assets/08ae8b9c-c84d-4b05-98d2-7edf23a80a97)
 
I was confused about what project I should do for my first Data Analysis Project. I didn't want a basic database or cliche ones. So I asked myself, what data do you want to do an insight on? I remembered how I always hated prejudices about Egypt and Egyptians. So, I wanted to get an insight on Egypt to answer some questions that I wanted to ask: 
1. Has Egypt’s **population growth only surged in recent years**, or has it been steadily increasing over time?
2. How has the Population of the **3 demographic age groups changed over the years**?
3. Did **female Employment affect** the total employment scene?
4. How have employment trends evolved across different sectors like **agriculture, services, and industry**?
5. Has there been a **noticeable migration from rural areas to urban cities** in Egypt over the years?
6. How did Egypt's **energy sources change over the year**?
 
## Dashboard File 

[You can check the dashboard Excel file from here](Project_File)

## Excel skills used 
- 🧹 **Data Cleaning & Filtering**  
- 🧮 **Handling Missing Values With Formulas**  
- 📊 **Named Ranges & Interactive Charts**  
- ✅ **Data Validation**  
  
## Egypt Dataset Used 
A huge thanks to the incredible team at World Bank Data 🙏 for providing open access to high-quality data. Their work makes projects like this possible for data enthusiasts and learners alike. 
[Explore the original dataset here](Resources) 
 
## Dashboard build  
### 🧹 **Data Cleaning & Filtering**  
  
I started by reviewing all available indicators and filtered out any that didn’t have at least 30 years of consistent data. This helped ensure that the trends I analyzed were reliable and meaningful.  
![Cleaning](https://github.com/user-attachments/assets/9eb40e25-165f-4918-8317-a499cd8b1b12)  
I also renamed and organized the columns to make them easier to work with during the analysis and dashboard creation.  
![CallData](https://github.com/user-attachments/assets/ff43ace6-3ba3-46c4-9182-6408247d2f7c)

### 🧮 **Handling Missing Values With Formulas**  

Some indicators had missing values scattered throughout the years. Instead of removing them or filling them in manually, I used formulas to automatically fill in the missing values by referencing the nearest known data points. This kept the data continuous and allowed the charts to reflect more accurate trends.  
```
{
=IF(B3<>0, B3, FORECAST.LINEAR(A2, FILTER(B:B, B:B<>0), FILTER(A:A, B:B<>0)))
}
```  
![FillingData](https://github.com/user-attachments/assets/7827a88d-370a-4a96-8c35-ef208e4c7905)  
  
### 📊 **Named Ranges & Interactive Charts**  
  
```
{
=OFFSET('Call Data here'!$BD$1,1,0,'Call Data here'!$BC$1-1,1)
#"$BD$1": is the starting cell of the named range, "$BC$1": is the count of the number of cells in a column
}
```  
To make the dashboard more dynamic, I used named ranges to create charts that respond to user selections. This allowed me to switch between different scenarios (like comparing two datasets) without duplicating charts or making a second dashboard. It made the dashboard more flexible and easier to explore.  
![Dynamic Charts](https://github.com/user-attachments/assets/e1ff8743-ded2-4994-98c2-0113a6de87c8)  

### ✅ **Data Validation**  
  
To keep the dashboard user-friendly and error-free, I applied data validation rules across key input cells. This helped prevent accidental changes, ensured dropdowns worked as expected, and kept the entire workbook clean and consistent during analysis.

## Conclusion  
I created this dashboard to showcase insights on some prejudices about Egypt. Utilizing data from World Bank data, this dashboard allows users to know with real-world data how numbers actually change throughout Egypt's history from the 1960s. It was an amazing experience to learn multiple tricks along the way and a new way of thinking using numbers.
