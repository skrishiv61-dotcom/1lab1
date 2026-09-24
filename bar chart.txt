import matplotlib.pyplot as plt
import numpy as np

# Data
subjects = ['Python', 'Java', 'C++', 'SQL', 'R']
marks = [90, 75, 80, 85, 70]

# Create color gradient
colors = plt.cm.viridis(np.linspace(0, 1, len(subjects)))

# Create bar chart
plt.bar(subjects, marks, color=colors)

# Labels and title
plt.xlabel("Subjects")
plt.ylabel("Marks")
plt.title("Student Marks - Gradient Bar Chart")

# Display values
for i, value in enumerate(marks):
    plt.text(i, value + 1, str(value), ha='center')

plt.show()
