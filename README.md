# ActBlue analysis

## Who did this?

This is a product of the Center for Public Integrity's data team. It was created by Chris Zubak-Skees with portions based on work by Joe Yerardi. The analysis was informed by questions posed by political reporter Carrie Levine.

## What's here?

* [Donors](donors.ipynb) — A profile of ActBlue's donors.

## Why did we do this?

What does it mean when one organization raises $2 billion for democrats? The Center set out to answer that question.

## How did we do it?

This analysis relied on a PostgreSQL database of more than 289,500 campaign finance filings loaded by the Center using [fec-loader](https://github.com/PublicI/fec-loader). These were analyzed using SQL, Pandas and Jupyter notebook software.

The notebook was developed on MacOS 10.13.3 with `git`, `virtualenv` and Python 3 installed. These instructions are specific to that environment, but should be adaptable to others:

```sh
git clone https://github.com/PublicI/actblue-analysis.git
cd actblue-analysis
virtualenv -p python3 .
source bin/activate
pip3 install -r requirements.txt
cp config.json.example config.json
jupyter lab
```

To connect to a PostgreSQL database with campaign finance records, update the values in [config.json](config.json) to the correct hostname and password.
