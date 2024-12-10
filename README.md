# Intro to Pandas (Python Data Handling Library)
**Definition/Overview:** Pandas is an open source coding library for Python, providing tools for data manipulation and analysis.

**Installation:** The easiest way to install Python is through the [pip](https://pypi.org/project/pip/) tool: simply use the `pip install pandas` or `pip3 install pandas` command, in terminal.

**Data Structures:** Pandas is dependent on two primary data handling structures: 'Series' and 'Data Frame'.

| Structure | Definition | Example |
| ------ | ------ | ---------- |
| Series | 1D Array (can store any 1 data type) | `s = pand.Series([0, 1, 2, 3])` |
| Data Frame | 2D Array (can use different data types) | `dframe = pand.DataFrame({'a': [0, 1], 'b': [2, 3]})` |

**Data Processing (4 Formats, with examples):**  

* JSON
  + Read Operation: `dframe = pand.read_json('example.json')`
  + Write Operation: `dframe.to_json('new_write.json')`
* CSV
  + Read Operation: `dframe = pand.read_csv('example.csv')`
  + Write Operation (with row labels unadded to output file): `dframe.to_csv('new_write.csv', index=False)`
* Excel (XLSX)
  + Read Operation: `dframe = pand.read_excel('example.xlsx')`
  + Write Operation (with row labels unadded to output file): `dframe.to_excel('new_write.xlsx', index=False)`
* Parquet (Apache open source solution)
  + Read Operation: `dframe = pand.read_parquet('example.parquet')`
  + Write Operation: `dframe.to_parquet('new_write.parquet')`
<br /><br />

**Initial Data Analysis/Exploration Tools:**

| Function or Property | Purpose |
| ------- | ------- |
| `dframe.head()` | Returns an amount of rows defined by the user, beginning at the start of the data. |
| `dframe.tail()` | Returns an amount of rows defined by the user, beginning at the bottom of the data. |
| `drame.describe()` | Returns descriptive, summary statistics for specified columns. |  
| `df.columns` | Returns column names/labels. |  
| `df.dtypes` | Returns column data types. |
| `df.isnull().sum()` | Returns the number of missing items/values for specified columns. |
