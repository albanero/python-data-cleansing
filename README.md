# Python Data Cleansing
# TOC 
* [Problem Statement](#problem-statement)
* [Names Contact Info Data Set](#names-contact-info-data-set)
* [Technical Instructions](#technical-instructions)
* [Submit Your Assignment](#submit-your-assignment)
* [Bonus Points (Extra Credit)](#bonus-points-extra-credit)

# Problem Statement
Given the [Names Contact Info Data Set](#names-contact-info-data-set), we want to cleanse, transform, and report on the data.

## Cleansing
Eliminate a record if it has any of the following data quality issues:
* Both the `first_name` and `last_name` are null/empty.

## Transformations
Transform the data as follows:
* Remove any non-alphanumeric characters.
* Convert all fields to uppercase.
* Convert `gender` from `Male|Female` to `M|F`.
* For the `phone`, convert to 10 digits by removing:
 * Punctuation: `()-`
 * The Country code: `+1`

## Reporting
The output should be in a `.txt` file, and should include:
* For each column, calculate:
  * `count`
  * `min`
  * `max`
  * The percentage of nulls.
* For the `first_name` and `last_name`:
  * The total # of occurrences for each name.

# Names Contact Info Data Set
In the `data` directory, the Names Contact Info Data Set (`names-contact-info.csv`) has the following columns:
* `id`
* `first_name`
* `last_name`
* `email`
* `gender`
* `address`
* `city`
* `state`
* `postal_code`
* `phone`

# Technical Instructions
* Please use PySpark DataFrames.
* Please comment your code.

# Submit Your Assignment
Please submit your assignment as follows:
* Upload your code along with your output `.txt` file to your folder on the 
[`albanero_python_data_cleansing` Google Drive](https://drive.google.com/drive/u/1/folders/13mMEIRSd9hh4skGGFEo-19agc0fdlvAy).

* Email [rahul.kumar@albanero.io](mailto:rahul.kumar@albanero.io) and [tom.marrs@albanero.io](mailto:tom.marrs@albanero.io) to inform us that you have completed your assignment.

# Bonus Points (Extra Credit)
You get extra credit for including either or both of the following:
* Package the project into a `.zip` or `.egg` file and run it with `spark-submit`
* Put the code into a Jupyter Notebook that's connected to PySpark and run it from there.
