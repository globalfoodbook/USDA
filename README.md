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
