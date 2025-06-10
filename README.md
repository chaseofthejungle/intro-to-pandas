# Intro to Pandas (Python Data Handling Library)
**Definition/Overview:** [Pandas](https://pandas.pydata.org/) is an open source coding library for Python, providing tools for data manipulation and analysis. The easiest way to install Python is through the [pip](https://pypi.org/project/pip/) tool: simply use the `pip install pandas` or `pip3 install pandas` command, in terminal.

<hr />

#### Table of Contents:

1. [Data Structures](#data-structures)
2. [Data Processing Formats](#data-processing)
3. [Initial Data Analysis/Exploration (for Data Frames)](#data-analysis)
4. [Data Reading/Selection (for Data Frames)](#data-reading)
5. [Supplemental Resources](#supplemental)
  
<hr />
  
## 1. <a name="data-structures">Data Structures</a>
  
Pandas is dependent on *two* primary data handling structures:
  
| Structure | Definition | Example |
| ------ | ------ | ---------- |
| Series | 1D Array (can store any 1 data type) | `s = pand.Series([0, 1, 2, 3])` |
| Data Frame | 2D Array (can use different data types) | `dframe = pand.DataFrame({'a': [0, 1], 'b': [2, 3]})` |

<hr />

## 2. <a name="data-processing">Data Processing Formats</a>
  
* [**JSON**](https://docs.python.org/3/library/json.html)
  + Read Operation: `dframe = pand.read_json('example.json')`
  + Write Operation: `dframe.to_json('new_write.json')`
* [**CSV**](https://docs.python.org/3/library/csv.html)
  + Read Operation: `dframe = pand.read_csv('example.csv')`
  + Write Operation (with row labels unadded to output file): `dframe.to_csv('new_write.csv', index=False)`
* [**Excel (XLSX)**](https://www.microsoft.com/en-us/microsoft-365/excel)
  + Read Operation: `dframe = pand.read_excel('example.xlsx')`
  + Write Operation (with row labels unadded to output file): `dframe.to_excel('new_write.xlsx', index=False)`
* [**Parquet (Apache open source solution)**](https://parquet.apache.org/)
  + Read Operation: `dframe = pand.read_parquet('example.parquet')`
  + Write Operation: `dframe.to_parquet('new_write.parquet')`
  
<hr />
  
## 3. <a name="data-analysis">Initial Data Analysis/Exploration (for Data Frames)</a>
  
| Function or Property | Purpose |
| ------- | ------- |
| `dframe.head()` | Returns an amount of rows defined by the user, beginning at the start of the data. |
| `dframe.tail()` | Returns an amount of rows defined by the user, beginning at the bottom of the data. |
| `dframe.describe()` | Returns descriptive, summary statistics for specified columns. |  
| `dframe.columns` | Returns column names/labels. |  
| `dframe.dtypes` | Returns column data types. |
| `dframe.isnull().sum()` | Returns the number of missing items/values for specified columns. |
  
<hr />
  
## 4. <a name="data-reading">Data Reading/Selection (for Data Frames)</a>
  
| Function or Property | Purpose |
| ------- | ------- |
| `dframe['col_name')]` | Reads/selects a column. |
| `dframe[['col_name1', 'col_name2']]`| Reads/selects more than one specified column. |
| `dframe.iloc[0:4]` | Reads/selects rows by provided indices. |
| `dframe[dframe['col_name'] >= 5]` | Reads/selects rows according in response to provided conditional test. |

<hr />
  
## 5. <a name="supplemental">Supplemental Resources</a>
  
* *[Official pandas Installation Page](https://pandas.pydata.org/docs/getting_started/install.html)*
* *[Python Networking Scripts Guide](https://github.com/chaseofthejungle/python-networking-scripts)*
* *[Python-Based Intrusion Detection System](https://github.com/chaseofthejungle/python-ids)*
