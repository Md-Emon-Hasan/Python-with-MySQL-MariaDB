# Python with MySQL & MariaDB

![MySQL](https://img.shields.io/badge/MySQL-compatible-4479A1?logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-compatible-003545?logo=mariadb&logoColor=white)
![PyMySQL](https://img.shields.io/badge/driver-PyMySQL-4B8BBE)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

A beginner-friendly collection of Python scripts for learning how to connect to MySQL or MariaDB and run common SQL operations. The numbered examples progress from database setup and CRUD queries to filtering, joins, and aggregate functions.

> These are standalone learning examples, not a packaged application. Most scripts connect to a local database named `school`; connection settings are currently written directly in each script.

## Contents

- [What you will learn](#what-you-will-learn)
- [Requirements](#requirements)
- [Setup](#setup)
- [Examples](#examples)
- [Database tables used by the examples](#database-tables-used-by-the-examples)
- [Safe usage notes](#safe-usage-notes)
- [Contributing](#contributing)
- [License](#license)
- [Connect with me](#connect-with-me)

## What you will learn

- Connecting Python to MySQL and MariaDB with PyMySQL
- Creating a database and table, then inserting, selecting, updating, and deleting rows
- Sorting, limiting, searching, and filtering query results
- Using `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and join conditions
- Applying `BETWEEN`, `IN`, `DISTINCT`, `GROUP BY`, `MIN`, `MAX`, `SUM`, `AVG`, and `COUNT`

## Requirements

- Python 3
- A running MySQL or MariaDB server and a database user with permission to create and modify tables
- The PyMySQL driver

Install the dependency:

```bash
python -m pip install PyMySQL
```

## Setup

1. Clone the repository and enter its directory:

   ```bash
   git clone https://github.com/Md-Emon-Hasan/Python-with-MySQL-MariaDB.git
   cd Python-with-MySQL-MariaDB
   ```

2. Open the scripts you want to run and update the connection arguments to match your local server. Most scripts use `host='localhost'`, `user='root'`, an empty password, and `database='school'`. Change these values if your server uses different credentials.

3. Start your MySQL or MariaDB server. Run the numbered setup and CRUD examples in order:

   ```bash
   python "1 Database and Connection.py"
   python "2 Create Table.py"
   python "3 Insert Query.py"
   python "4 Select Query.py"
   ```

   Script 1 creates the `school` database. Script 2 creates a `student` table. The insert and select examples then use that table. The remaining CRUD scripts (`5 Delete Query.py` and `6 Update Query.py`) also work with it.

4. Run any other example with Python, quoting the filename because it contains spaces. For example:

   ```bash
   python "7 Order by and Limit.py"
   ```

The scripts are separate exercises; there is no central application entry point or `requirements.txt` in this repository.

## Examples

| File | Topic | Tables referenced |
| --- | --- | --- |
| `1 Database and Connection.py` | Connect and create the `school` database | Creates database |
| `2 Create Table.py` | Create the student table | `student` |
| `3 Insert Query.py` | Insert one student; includes a commented multi-row example | `student` |
| `4 Select Query.py` | Select and display student records | `student` |
| `5 Delete Query.py` | Delete a student by ID | `student` |
| `6 Update Query.py` | Update a student record | `student` |
| `7 Order by and Limit.py` | Sort results and limit rows | `student` |
| `8 Searching and Filter Data.py` | Search by student name and class | `student` |
| `9 INNER JOIN.py` | Inner join state and country records | `state`, `country` |
| `10 LEFT JOIN.py` | Left join state and country records | `state`, `country` |
| `11 RIGHT JOIN.py` | Right join users and orders | `user`, `orders` |
| `12 EQUI JOIN.py` | Join state and country with a matching-key condition | `state`, `country` |
| `13 Self Join and Full Outer.py` | Self-join a category hierarchy | `cat` |
| `14 BETWEEN Operators.py` | Filter IDs within a range | `state` |
| `15 Use of MAX and MIN Functions.py` | Find the maximum order amount; includes a commented minimum query | `orders` |
| `16 GROUP BY Statement.py` | Count records grouped by department name | `operators` |
| `17 Distinct Keyword.py` | Return unique department names | `operators` |
| `18 SUM () Function.py` | Sum order amounts | `orders` |
| `19 AVG ().py` | Average order amount | `orders` |
| `20 Count Function.py` | Count order records | `orders` |
| `21 IN or NOT.py` | Select orders whose IDs match a list | `orders` |

## Database tables used by the examples

Only the `student` table is created by the scripts in this repository. The join, category, state/country, order, and operator examples expect additional tables and columns to exist in the `school` database. No schema or sample data for those tables is included, so create and populate the required tables before running those exercises. Check each script's SQL query for the exact column names it uses.

## Safe usage notes

- Use a database account with only the permissions needed for the exercise. Avoid using a privileged account for applications.
- Do not commit real passwords or other secrets. For personal use, replace the example credentials locally; for a real application, load credentials from environment variables or a secret manager.
- Use parameterized queries for values supplied by users. Most examples that pass values as query parameters demonstrate this pattern. `8 Searching and Filter Data.py` currently builds SQL by concatenating input, which is unsafe for untrusted input; update it to use `%s` placeholders before adapting it for real use.
- These scripts are intended for learning. They use simple error handling and do not consistently close cursors or connections.

## Contributing

Improvements and additional examples are welcome:

1. Fork the repository.
2. Create a branch for your change.
3. Make and commit your changes.
4. Push the branch and open a pull request with a short description of the update.

## License

This project is distributed under the [MIT License](LICENSE).

## Connect with me

- 🌐 **Portfolio:** [emonlabs-ai.hitechparks.com](https://emonlabs-ai.hitechparks.com)
- 💻 **GitHub:** [Md-Emon-Hasan](https://github.com/Md-Emon-Hasan)
- 💼 **LinkedIn:** [Md Emon Hasan](https://www.linkedin.com/in/md-emon-hasan-695483237/)
- 🤗 **Hugging Face:** [emonHasan01](https://huggingface.co/emonHasan01)
- 📧 **Email:** [emon.mlengineer@gmail.com](mailto:emon.mlengineer@gmail.com)
- 📱 **WhatsApp:** [+8801834363533](https://wa.me/8801834363533)
