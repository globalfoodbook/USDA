# USDA
Take note of plain and c formats for postgressql (pg_restore)

# Examples

## Export

### C Format

```pg_dump --format=custom  db_name > nutrition_sr<number>_c.dump```

### Plain Format

```pg_dump --format=plain  db_name > nutrition_sr<number>_plain.dump```

## Import / Restore

### Plain Format

``` heroku pg:backups restore 'https://raw.githubusercontent.com/globalfoodbook/USDA-DATA/master/nutrition_sr26_plain.dump' DATABASE_URL --app APP --confirm APP ```

### C Format

``` heroku pg:backups restore 'https://raw.githubusercontent.com/globalfoodbook/USDA-DATA/master/nutrition_sr26_c.dump' DATABASE_URL --app APP --confirm APP ```

### Import ElephantSQL
NB: Plain Format Used http://elephantsql.com

``` psql postgres://<username>:<password>@pellefant.db.elephantsql.com:5432/<db_name> < nutrition_sr<number>_plain.dump ```

## Links
USDA Nutrition Database: [http://www.ars.usda.gov/Services/docs.htm?docid=8964](http://www.ars.usda.gov/Services/docs.htm?docid=8964)

[Importing and Exporting Heroku Postgres Databases with PG Backups](https://devcenter.heroku.com/articles/heroku-postgres-import-export)

[ElephantSQL Documentation](http://www.elephantsql.com/docs/index.html)

Updates for nutrition label: [healthy food recipes](http://globalfoodbook.com) 
