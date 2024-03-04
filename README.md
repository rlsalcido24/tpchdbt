# TPC-H on DBSQL

This project is an adaption of [dbt-tpch](https://github.com/clausherther/dbt-tpch) for Databricks SQL

### Getting started

- Install dbt
- Create a profile in `~/.dbt/profiles.yml`

```
shant_test:
  outputs:
    dev:
      type: databricks
      schema: shant
      host: adb-2548836972759138.18.azuredatabricks.net
      http_path: /sql/1.0/endpoints/071969b1ec9a91ca
      token: dapiBLAHBLAH
  target: dev
```

- Install the `dbt-databricks` package using pip
- Run these commands:

```
python3 -m venv dbt-bugbash-env
source dbt-bugbash-env/bin/activate
pip install DOWNLOAD_PATH/dbt_databricks-1.0.0rc1-py3-none-any.whl
dbt deps
```
- Now run `dbt run`
