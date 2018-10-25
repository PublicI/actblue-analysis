# ActBlue analysis

## Who did this?

This is an analysis from the Center for Public Integrity's data team in partnership with FiveThirtyEight. It was created by Chris Zubak-Skees. The analysis was informed by questions posed by political reporter Carrie Levine.

## What's here?

* [Analysis](analysis.ipynb) - An analysis of ActBlue and other FEC filings.
* [Data](data) - Spreadsheets produced by the analysis.

## Why did we do this?

What does it mean when one organization raises more than $2.9 billion for democrats? The Center set out to answer that question.

## How did we do it?

This analysis relied on a PostgreSQL database of more than 289,500 campaign finance filings loaded by the Center using [fec-loader](https://github.com/PublicI/fec-loader). These were analyzed using SQL, Pandas and Jupyter notebook software.

The notebook was developed on MacOS 10.13 with `git`, `pipenv` and Python 3 installed. These instructions are specific to that environment, but should be adaptable to others:

```sh
git clone https://github.com/PublicI/actblue-analysis.git
cd actblue-analysis
pipenv install
pipenv shell
python -m ipykernel install --user --name=actblue-analysis
jupyter lab
```

Query results are persisted to [Pickle](https://docs.python.org/3/library/pickle.html) files, so the notebook can be run without access to the database.

If you do have access to a PostgreSQL database of campaign finance records in the correct schema and want to modify the queries, copy config.json.example to config.json, then update the values in [config.json](config.json) to the correct hostname and password.
