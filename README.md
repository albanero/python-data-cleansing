# Python Data Cleansing
# TOC 
* [Problem Statement](#problem-statement)
* [Names Contact Info Data Set](#names-contact-info-data-set)
* [Instructions](#instructions)
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
The end result should be in a `.txt` file in the `output` directory, and should include:
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

# Instructions
* Please use PySpark DataFrames,
* Please check in your code under the `code` directory for review.
* Please comment your code.

# Bonus Points (Extra Credit)
* Package the project into a `.zip` or `.egg` file and run it with `spark-submit`
* Put the code into a Jupyter Notebook that's connected to PySpark and run it from there.
