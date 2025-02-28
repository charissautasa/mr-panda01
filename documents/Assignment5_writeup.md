# Assignment 5 Write-Up

## Project Overview
This project involves analyzing and merging datasets related to superheroes and their publishers. The goal is to understand how different variables affect the merging process and how to handle compound keys.

## Modifications Based on Feedback
- **Displaying the New Dataset**: Added code to print the modified DataFrames to show the changes clearly.
- **Handling Compound Keys**: Enhanced the explanation and provided a clear example of merging using a compound key.
- **Variables Explanation**: Expanded the explanation of each variable and provided relationships and analysis.

## Code Implementation
```python
# Original publishers DataFrame
publishers = pd.DataFrame({
    "publisher": ["DC", "Marvel", "Image"],
    "year_founded": [1934, 1939, 1992]
})

# Add a second entry for Marvel with a different founding year
new_publisher_row = pd.DataFrame({"publisher": ["Marvel"], "year_founded": [1961]})
publishers = pd.concat([publishers, new_publisher_row], ignore_index=True)

# Add a new superhero with a conflicting alignment (Magneto as "good")
new_superhero_row = pd.DataFrame({
    "name": ["Magneto"],
    "alignment": ["good"],
    "gender": ["male"],
    "publisher": ["Marvel"]
})

superheroes = pd.concat([superheroes, new_superhero_row], ignore_index=True)

# Display the modified DataFrames
print("Modified Superheroes DataFrame:")
print(superheroes)
print("\nModified Publishers DataFrame:")
print(publishers)