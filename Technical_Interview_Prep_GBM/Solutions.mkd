## Solutions

### SQL

#### Exercise 1:
```sql
SELECT products.category, AVG(customers.age) AS avg_age
FROM customers
JOIN purchases ON customers.customer_id = purchases.customer_id
JOIN products ON purchases.product_id = products.product_id
WHERE purchases.purchase_date >= DATE('now', '-1 month')
GROUP BY products.category;
```

#### Exercise 2:
```sql
SELECT products.category, products.product_id, COUNT(*) AS purchase_count
FROM purchases
JOIN products ON purchases.product_id = products.product_id
WHERE purchases.purchase_date >= DATE('now', '-30 days')
GROUP BY products.product_id
ORDER BY purchase_count DESC
LIMIT 5;
```

### Data Manipulation

#### Exercise 1:
```python
# Step 1: Remove duplicates based on review_id and user_id
df = df.drop_duplicates(subset=['review_id', 'user_id'])

# Step 2: Handle missing values
df['review_text'] = df['review_text'].fillna('No review provided')  # Fill missing reviews with a placeholder
df['rating'] = df['rating'].fillna(df['rating'].mean())  # Replace missing ratings with the mean rating

# Step 3: Normalize text data (convert to lowercase and remove punctuation)
df['review_text'] = df['review_text'].str.lower().str.replace('[^\w\s]', '', regex=True)

# Display cleaned data
print(df)
```

```{r}
# Step 1: Remove duplicates based on review_id and user_id
data_clean <- data %>%
  distinct(review_id, user_id, .keep_all = TRUE)

# Step 2: Handle missing values
data_clean$review_text[is.na(data_clean$review_text)] <- "No review provided"
data_clean$rating[is.na(data_clean$rating)] <- mean(data_clean$rating, na.rm = TRUE)

# Step 3: Normalize text data (convert to lowercase and remove punctuation)
data_clean$review_text <- str_to_lower(data_clean$review_text)
data_clean$review_text <- str_remove_all(data_clean$review_text, "[^\\w\\s]")

# Display cleaned data
print(data_clean)
```

#### Exercise 2:
```python
# Handle outliers using IQR method
df_clean_iqr = handle_outliers(df, method='IQR', column='age')

# Handle outliers using Z-score method
df_clean_zscore = handle_outliers(df, method='Z-score', column='age')

print("Data without IQR outliers:")
print(df_clean_iqr)
print("\nData without Z-score outliers:")
print(df_clean_zscore)
```

```{r}
# Handle outliers using IQR method
df_clean_iqr <- handle_outliers(data, method = 'IQR', column = 'age')

# Handle outliers using Z-score method
df_clean_zscore <- handle_outliers(data, method = 'Z-score', column = 'age')

cat("Data without IQR outliers:\n")
print(df_clean_iqr)

cat("\nData without Z-score outliers:\n")
print(df_clean_zscore)
```

### Programming

#### Exercise 1:
```python
def intersection(arr1, arr2):
    # Initialize indices for both arrays
    i, j = 0, 0
    intersection = []
    
    # Traverse both arrays using the indices
    while i < len(arr1) and j < len(arr2):
        if arr1[i] == arr2[j]:
            # If the elements are equal, add to the intersection
            intersection.append(arr1[i])
            i += 1
            j += 1
        elif arr1[i] < arr2[j]:
            # If element in arr1 is smaller, move index i forward
            i += 1
        else:
            # If element in arr2 is smaller, move index j forward
            j += 1
    
    return intersection
```

#### Exercise 2:
```python
def max_sum(nums):
    # Edge case: If the list is empty, return 0
    if not nums:
        return 0
    
    # Edge case: If the list has only one element, return that element
    if len(nums) == 1:
        return nums[0]
    
    # Initialize the 'include' and 'exclude' variables
    include = 0
    exclude = 0
    
    for num in nums:
        # Calculate the new 'include' and 'exclude' values
        new_include = exclude + num
        new_exclude = max(include, exclude)
        
        # Update the 'include' and 'exclude' values
        include = new_include
        exclude = new_exclude
    
    # The result will be the maximum of 'include' and 'exclude'
    return max(include, exclude)
```
