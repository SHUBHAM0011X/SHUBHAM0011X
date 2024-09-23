import pandas as pd
import matplotlib.pyplot as plt

# Sample data: bone density based on daily calcium intake
data = {
    'Calcium Intake (mg)': [500, 700, 800, 900, 1200, 1500, 2000],
    'Bone Density (g/cm^2)': [0.8, 0.85, 0.9, 0.95, 1.0, 1.1, 1.2]
}

# Create a DataFrame
df = pd.DataFrame(data)

# Calculate mean and median
mean_bone_density = df['Bone Density (g/cm^2)'].mean()
median_bone_density = df['Bone Density (g/cm^2)'].median()

print(f"Mean Bone Density: {mean_bone_density}")
print(f"Median Bone Density: {median_bone_density}")

# Visualize the data with a box plot
plt.boxplot(df['Bone Density (g/cm^2)'])
plt.title('Box Plot of Bone Density')
plt.ylabel('Bone Density (g/cm^2)')
plt.show()
