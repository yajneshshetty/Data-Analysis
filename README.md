# Dataset

The dataset is generated using Python with the help of the following libraries:

Pandas: Used for data manipulation and creating DataFrames.
NumPy: Used for generating random numbers and creating arrays.
Faker: Used for generating fake data such as names, job titles, and dates.
Here's a breakdown of how the dataset is generated:

Initialization: First, necessary libraries are imported - Pandas, NumPy, and Faker. Faker is initialized to generate fake data.

Data Generation: A dictionary named data is created to store the generated data. Each key in the dictionary represents a column name, and the corresponding value is a list containing the generated data for that column.

Employee ID: A list of employee IDs is generated using a list comprehension with the format 'EMP' + str(i).zfill(4) to ensure IDs are formatted with leading zeros (e.g., EMP0001).

Employee Name, Age, Gender, Department, Position, Years of Experience, Salary, Performance Rating, Education Level, Hired Date: Fake data is generated for these columns using the fake object from the Faker library. For each column, a loop generates random data based on predefined distributions or choices. For instance, fake.name() generates a random name, random.randint(22, 65) generates a random age between 22 and 65, and fake.date_between(start_date='-5y', end_date='today') generates a random date within the last 5 years up to today's date.

Creating DataFrame: The dictionary data is used to create a Pandas DataFrame df using the pd.DataFrame() function.

Export to Excel: Finally, the DataFrame is exported to an Excel file named 'hr_consultancy_dataset.xlsx' using the to_excel() method. Each column of the DataFrame corresponds to a column in the Excel file, and the index (row numbers) are excluded from the exported Excel file by setting index=False.
