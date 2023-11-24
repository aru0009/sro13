1
import pandas as pd

# Create a synthetic dataset
data = {
'Age': [25, 30, 35, 40, 22, 28, 32, 38, 21, 27],
'Weight': [65, 72, 68, 75, 60, 68, 70, 80, 58, 66],
'Height': [170, 175, 180, 165, 160, 172, 178, 168, 163, 175],
'BloodPressure': [120, 130, 118, 122, 115, 128, 135, 118, 125, 132],
}

# Create a DataFrame
full_health_data = pd.DataFrame(data)

# Set display options to show all columns and rows
pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)

# Display summary statistics of the dataset
print(full_health_data.describe())

2
import pandas as pd
import numpy as np

# Create a DataFrame manually
data = {
'Age': [25, 30, 35, 40, 45, 50, 55, 60, 65, 70],
'Max_Heart_Rate': [180, 175, 190, 200, 185, 175, 195, 205, 190, 180]
}

full_health_data = pd.DataFrame(data)

# Calculate the 10th percentile of the "Max_Heart_Rate" column
max_heart_rate = full_health_data["Max_Heart_Rate"]
percentile10 = np.percentile(max_heart_rate, 10)

print(percentile10)

3
import pandas as pd
import numpy as np

# Create a DataFrame manually
data = {
'Height': [160, 165, 170, 175, 180, 185, 190, 195, 200, 205],
'Weight': [55, 60, 65, 70, 75, 80, 85, 90, 95, 100]
}

full_health_data = pd.DataFrame(data)

# Calculate the standard deviation for each column
std_height = np.std(full_health_data['Height'])
std_weight = np.std(full_health_data['Weight'])

print(f"Standard Deviation of Height: {std_height}")
print(f"Standard Deviation of Weight: {std_weight}")

4
import pandas as pd
import numpy as np

# Create a DataFrame manually
data = {
'Steps': [8000, 8500, 9000, 9500, 10000, 10500, 11000, 11500, 12000, 12500],
'Calories_Burned': [300, 310, 320, 330, 340, 350, 360, 370, 380, 390]
}

health_data = pd.DataFrame(data)

# Calculate the variance for each column
var_steps = np.var(health_data['Steps'])
var_calories = np.var(health_data['Calories_Burned'])

print(f"Variance of Steps: {var_steps}")
print(f"Variance of Calories Burned: {var_calories}")

5
import sys
import matplotlib
matplotlib.use('Agg')

import pandas as pd
import matplotlib.pyplot as plt

# Create a DataFrame manually
data = {
'Average_Pulse': [70, 75, 80, 85, 90, 95, 100, 105, 110, 115],
'Calorie_Burnage': [150, 160, 170, 180, 190, 200, 210, 220, 230, 240]
}

health_data = pd.DataFrame(data)

# Scatter plot
health_data.plot(x='Average_Pulse', y='Calorie_Burnage', kind='scatter')
plt.title('Average Pulse vs Calorie Burnage')
plt.xlabel('Average Pulse')
plt.ylabel('Calorie Burnage')

# Save the plot to a file
plt.savefig(sys.stdout.buffer)
sys.stdout.flush()

6
import pandas as pd

# Create a DataFrame manually
data = {
'Blood_Pressure': [120, 130, 110, 125, 140, 115, 135, 130, 125, 120],
'Cholesterol': [180, 200, 160, 190, 210, 170, 200, 195, 185, 180],
'BMI': [22, 25, 21, 23, 26, 20, 24, 25, 22, 23]
}

full_health_data = pd.DataFrame(data)

# Calculate the correlation matrix
corr_matrix = round(full_health_data.corr(), 2)

print("Correlation Matrix:")
print(corr_matrix)

7
import sys
import matplotlib
matplotlib.use('Agg')

import pandas as pd
import matplotlib.pyplot as plt

# Create a DataFrame manually
beach_data = {
'Sunscreen_Use': [30, 40, 50, 60, 70, 80, 90, 100, 110, 120],
'Skin_Burns': [20, 35, 50, 65, 80, 95, 110, 125, 140, 155]
}

beach_df = pd.DataFrame(data=beach_data)

# Scatter plot
beach_df.plot(x='Sunscreen_Use', y='Skin_Burns', kind='scatter')
plt.title('Sunscreen Use vs Skin Burns')
plt.xlabel('Sunscreen Use (minutes)')
plt.ylabel('Skin Burns')

# Save the plot to a file
plt.savefig(sys.stdout.buffer)
sys.stdout.flush()

# Calculate and print the correlation matrix
correlation_beach = beach_df.corr()
print("Correlation Matrix:")
print(correlation_beach)
