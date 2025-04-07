# Excel Project: Motorcycle Sales Analysis

![image](https://github.com/user-attachments/assets/e5274d65-e985-4cc0-9d08-827cd0e3be48)

## 📌 Introduction
This project provides a step-by-step guide to creating an interactive dashboard in Excel to analyze motorcycle purchase patterns using professional data analysis techniques. Here's what the initial dataset looks like:

![image](https://github.com/user-attachments/assets/22db5ed9-2a98-4374-8d36-dd0e12e3b6e9)

## 🔍 Step 1: Environment Setup
1. **Workbook Structure**:

   - `bike_buyers` (Original Dataset)

   - I created 3 additional sheets:
     - `Working Sheet` (Cleaned Data)
     - `Pivot Table` (Analysis)
     - `Dashboard` (Visual Panel)

   ![image](https://github.com/user-attachments/assets/1d7c870c-ef98-4b53-ba1a-c73c7c9b8d79)

3. 🛡️ **Data Protection**:
   - I copied all data from `bike_buyers` to `Working Sheet` to preserve the original data.

## 🧹 Step 2: Data Cleaning
1. **Duplicate Removal**:
   - Used the `Data > Remove Duplicates` option (26 duplicate records found and removed) ✔️

2. **Value Normalization**:

   ![image](https://github.com/user-attachments/assets/0b659534-162b-4925-80a8-7c4b2972c8d7)

   ![image](https://github.com/user-attachments/assets/ea9e53c0-4e59-4b98-a4c8-214b0840a5aa)

4. **Creating Age Ranges**:

   ![image](https://github.com/user-attachments/assets/180d31b6-441e-4ae0-9b92-74f74dd63131)

   - Added a column "Age Brackets" using the formula:

   ```excel
   =IF(L15>54,"Old",IF(L15>=31,"Middle Age",IF(L15<31,"Adolescent","Invalid")))
   ```

## 📐 Step 3: Pivot Tables
1. **Average Income by Gender**:
   - Rows: Gender  
   - Columns: Purchased Bike  
   - Values: Average of Income  

   ![image](https://github.com/user-attachments/assets/6e020412-7e80-4516-bb1d-6125041b6e90)

2. **Commute Distance per Customer**:
   - Rows: Commute Distance  
   - Values: Count of Purchased Bike  
   - (I adjusted "10+ Miles" → "More than 10 Miles")

   ![image](https://github.com/user-attachments/assets/e3f3a5bb-c009-469e-be36-e206bad57d80)

3. **Age Ranges**:
   - Rows: Age Brackets  
   - Values: Count of Purchased Bike  

   ![image](https://github.com/user-attachments/assets/414b556e-f671-48ca-88e3-8955dcbd078e)

4. **Traits of an Ideal Customer**:
   - Rows: Income, Commute Distance, and Cars  
   - Columns: Purchased Bike  
   - Values: Count of ID  

   ![image](https://github.com/user-attachments/assets/836df74c-c322-4979-bf32-29b64b3189c6)

## 📊📈 Step 4: Visualizations
1. **Column Charts**:
   - Created clustered column charts for each pivot table  
   - Added titles and professional formatting

   ![image](https://github.com/user-attachments/assets/8d11341d-7387-4902-b73e-13a0fdb5347c)
   ![image](https://github.com/user-attachments/assets/310328a5-fd3c-41a3-b5ae-2af157f42aae)
   ![image](https://github.com/user-attachments/assets/ac81373d-97f5-4b6d-bf5f-87e5850771b7)

2. **Doughnut Chart (Ideal Customer)**:
   - Type: Doughnut Chart  
   - Shows the relationship between Income, Cars, and Commute Distance
   - The relevant information to show here are the bigger squares/bars that hold the bigger values of people who bought and shows their same condition of salary, commute distance and if they own a vehicle

   ![image](https://github.com/user-attachments/assets/9772b40d-e5c5-4364-b844-d2c5ab72349e)

## 🖥️ Step 5: Interactive Dashboard
1. **Base Design**:
   - Removed gridlines (View > Show > Gridlines)  
   - Created a header using merged cells and professional formatting

   ![image](https://github.com/user-attachments/assets/1bca8ed9-02ae-4a64-a172-f0cecececf24)

2. **Chart Organization**:
   - Aligned charts using:  
     - `Shape Format > Align > Align Top/Left`  
   - Used proportional sizing

3. **Interactive Filters**:
   - Inserted slicers for:  
     1. Marital Status  
     2. Region  
     3. Education  
     4. Commute Distance  
   - Connected all filters to each pivot table

   ![image](https://github.com/user-attachments/assets/cc53aa7d-58c4-46eb-95c9-e47d4674905d)

## 🔎 Key Findings
- **Married vs Single**: Married buyers have higher average incomes.  
- **Age**: Middle-aged individuals (31–54) purchase more motorcycles.  
- **Distance**: Customers living 0 to 1 mile away purchase the most.  
- **Vehicles**: Customers without cars are more likely to buy.

## 💡 How to Customize
1. To change age ranges, modify the formula in the "Age Brackets" column.  
2. Add more filters via:  
   `PivotChart Analyze > Insert Slicer`  
3. Change colors using:  
   `Chart Design > Change Colors`
