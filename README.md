Here are detailed and easy-to-remember answers with brief explanations for each question:

---

### **Q8: R Program to Plot Different Diagrams**  

1. **Scatter Plot**:  
   A scatter plot shows the relationship between two variables using points.  
   ```R
   x <- c(1, 2, 3, 4, 5)
   y <- c(2, 4, 6, 8, 10)
   plot(x, y, main="Scatter Plot", xlab="X-axis", ylab="Y-axis", col="blue", pch=19)
   ```
   - `x` and `y` are the two variables.
   - `pch=19` makes the points solid.

2. **Histogram**:  
   A histogram represents the distribution of data by dividing it into intervals (bins).  
   ```R
   data <- c(5, 10, 15, 20, 25)
   hist(data, main="Histogram", xlab="Values", col="green", border="black")
   ```
   - `col` sets the bar colors, and `border` defines the border color.

3. **Pie Chart**:  
   A pie chart shows proportions of categories in a circular form.  
   ```R
   values <- c(30, 20, 50)
   labels <- c("A", "B", "C")
   pie(values, labels, main="Pie Chart", col=rainbow(length(values)))
   ```
   - `rainbow()` provides multiple colors for the pie slices.

4. **Heat Map**:  
   A heat map visualizes data in a matrix format with colors representing the values.  
   ```R
   matrix_data <- matrix(1:9, nrow=3)
   heatmap(matrix_data, main="Heat Map")
   ```
   - `matrix()` creates a numerical matrix.
   - `heatmap()` generates the visual.

---

### **Q9: Data Manipulation Functions in `dplyr`**

1. **`filter()`**:  
   Selects rows that meet a specific condition.  
   ```R
   library(dplyr)
   df <- data.frame(Age = c(20, 25, 30), Name = c("John", "Anna", "Mike"))
   filtered <- filter(df, Age > 20)
   print(filtered)
   ```
   - Here, rows where `Age > 20` are selected.

2. **`mutate()`**:  
   Adds new columns to the dataset without removing existing ones.  
   ```R
   mutated <- mutate(df, Age_in_5_years = Age + 5)
   print(mutated)
   ```
   - Adds a new column `Age_in_5_years`.

3. **`transmute()`**:  
   Adds new columns but keeps only the new ones in the result.  
   ```R
   transmuted <- transmute(df, Age_in_5_years = Age + 5)
   print(transmuted)
   ```
   - Only `Age_in_5_years` is returned.

4. **`distinct()`**:  
   Removes duplicate rows from the dataset.  
   ```R
   df_dup <- data.frame(Age = c(20, 25, 25), Name = c("John", "Anna", "Anna"))
   distinct_rows <- distinct(df_dup)
   print(distinct_rows)
   ```
   - Duplicates based on all columns are removed.

---

### **Q10: Calculating Statistical Metrics in R**  

#### **Explanation**:  
We use the following functions to calculate basic statistics:
- **Mean**: Average value.  
- **Median**: Middle value.  
- **Variance**: Measure of data spread.  
- **Standard Deviation**: Square root of variance.  
- **Covariance**: Shows how two variables change together.  
- **Correlation**: Strength of the relationship between two variables.

#### **Code**:  
```R
data <- c(1, 2, 3, 4, 5)

# Mean
mean_value <- mean(data)
print(paste("Mean:", mean_value))

# Median
median_value <- median(data)
print(paste("Median:", median_value))

# Variance
variance <- var(data)
print(paste("Variance:", variance))

# Standard Deviation
sd_value <- sd(data)
print(paste("Standard Deviation:", sd_value))

# Covariance
cov_value <- cov(data, data)  # Example with same data
print(paste("Covariance:", cov_value))

# Correlation
correlation <- cor(data, data)  # Example with same data
print(paste("Correlation:", correlation))
```

---

If you have any doubts or need more examples, feel free to ask! 😊
