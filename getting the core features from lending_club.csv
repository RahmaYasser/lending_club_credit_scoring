import pandas as pd

# Define the 20 core columns you want to keep
core_columns = [
    'id', 'loan_amnt', 'term', 'int_rate', 'grade', 'purpose',
    'fico_range_low', 'fico_range_high', 'annual_inc', 'dti',
    'revol_bal', 'revol_util', 'total_acc', 'open_acc',
    'loan_status', 'delinq_2yrs', 'inq_last_6mths', 'pub_rec',
    'home_ownership', 'addr_state'
]

# Read the original Lending Club CSV file
print("Reading original Lending Club dataset...")
df = pd.read_csv('lending_club_full.csv')

print(f"Original dataset shape: {df.shape}")
print(f"Original columns: {len(df.columns)}")

# Select only the core columns
df_core = df[core_columns]

print(f"Filtered dataset shape: {df_core.shape}")
print(f"Selected columns: {len(df_core.columns)}")

# Display first few rows to verify
print("\nFirst 5 rows of filtered dataset:")
print(df_core.head())

# Check for any missing columns
missing_cols = [col for col in core_columns if col not in df.columns]
if missing_cols:
    print(f"Warning: These columns are missing from the dataset: {missing_cols}")

# Save the filtered dataset
output_filename = 'lending_club_core_features.csv'
df_core.to_csv(output_filename, index=False)
print(f"\nFiltered dataset saved as: {output_filename}")

# Display basic statistics
print("\nDataset Summary:")
print(f"Total records: {len(df_core):,}")
print(f"Columns: {list(df_core.columns)}")
print(f"File size reduced from {len(df.columns)} to {len(df_core.columns)} columns")
