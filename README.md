This library provides utilities to generate mock data for testing purposes, including numbers, text, identifiers, and structured data.

## Modules Overview

# **Installation**
!pip install randomcontentgen


1. **Number Generator**
   - Generate random integers, floats, or numbers with custom ranges.
   - Example:
     ```python
     from randomcontent import generate_number
     generate_number(type="int", min=1, max=100)  # Generates an random integer between 1 and 100
     generate_number(type="probability") # Generates an random probability between 0 and 1
     generate_number(type="gaussian",mean=0, std_dev=1) # Generates an random number from Gaussian distribution

     ```

2. **Identifier Generator**
   - Generate unique identifiers like UUIDs, credit card numbers, or custom IDs.
   - Example:
     ```python
     from randomcontent import generate_identifier
     generate_identifier(type="uuid")  # Generates and random UUID-like string
     generate_identifier(type="email") # Generates an email address

     ```

3. **Text Generator**
   - Create random names, email addresses, or custom text strings.
   - Examples:
     ```python
     from randomcontent import generate_text
     generate_text(type="sentence", length=12)  # Generates a sentence
     generate_text(type="poem", num_lines=4)   # Generates a poem
     ```

4. **Structured Data Generator**
   - Generate structured mock data based on a schema definition.
   - Example:
     ```python
     from randomcontent import generate_structured_data, format_data
     schema = {"name": "random_name", "email": "random_email","age": "random_int(min=18, max=60)"}
     generate_structured_data(schema, count=5)  # List of 5 data rows
     ```

## Formatting Data
Structured data can be saved in JSON, CSV, or Parquet formats:
- Example:
  ```python
  from randomcontent import format_data
  format_data(data, format_type="json", file_name="data")  # Save as data.json
  format_data(data, format_type="csv", file_name="data")   # Save as data.csv
  format_data(data, format_type="parquet", file_name="data")  # Save as data.parquet
