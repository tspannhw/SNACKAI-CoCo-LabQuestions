### Answers to Questions



#### Identify Tables

* https://www.snowflake.com/en/product/features/horizon/

* https://docs.snowflake.com/en/sql-reference/info-schema

* https://docs.snowflake.com/en/user-guide/ui-snowsight-universal-search

* https://www.snowflake.com/en/product/use-cases/internal-marketplace/

* https://www.snowflake.com/en/developers/guides/internal-marketplace-intra-org-sharing/

* https://docs.snowflake.com/en/user-guide/sql-cortex-descriptions

* https://docs.snowflake.com/en/user-guide/ui-snowsight-cortex-descriptions


#### Find Tables

````
SELECT table_catalog, table_schema, table_name, row_count, comment
FROM DEMO.INFORMATION_SCHEMA.TABLES
WHERE table_schema != 'INFORMATION_SCHEMA'
ORDER BY row_count DESC;

````




