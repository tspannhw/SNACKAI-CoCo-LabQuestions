### Answers to Questions




#### Identify Tables

* https://www.snowflake.com/en/product/features/horizon/

* https://docs.snowflake.com/en/sql-reference/info-schema

* https://docs.snowflake.com/en/user-guide/ui-snowsight-universal-search






#### Make Your Tables Discoverable / Internal marketplace / Tagging / AI Descriptions

* https://docs.snowflake.com/en/sql-reference/account-usage/tag_references
  
* https://www.snowflake.com/en/product/use-cases/internal-marketplace/

* https://www.snowflake.com/en/developers/guides/internal-marketplace-intra-org-sharing/

* https://docs.snowflake.com/en/user-guide/sql-cortex-descriptions

* https://docs.snowflake.com/en/user-guide/ui-snowsight-cortex-descriptions




#### Find Tables



##### Note:  DEMO is the name of my database

````
SELECT table_catalog, table_schema, table_name, row_count, comment
FROM DEMO.INFORMATION_SCHEMA.TABLES
WHERE table_schema != 'INFORMATION_SCHEMA'
ORDER BY row_count DESC;

SELECT column_name, data_type, comment
FROM DEMO.INFORMATION_SCHEMA.COLUMNS
WHERE table_name = 'ICYMTA';

````



#### Streamlit


* https://streamlit.io/

* https://docs.streamlit.io/get-started/installation/streamlit-in-snowflake
  
* https://docs.snowflake.com/en/developer-guide/streamlit/getting-started/overview
  
* https://docs.snowflake.com/en/developer-guide/streamlit/app-development/creating-your-app

* https://docs.snowflake.com/en/developer-guide/streamlit/about-streamlit





#### Semantic View

* https://docs.snowflake.com/en/user-guide/views-semantic/overview

* https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst




#### Workspaces not Worksheets (SQL, Python, Jupyter Notebooks)

* https://docs.snowflake.com/en/user-guide/ui-workspaces-python

* https://docs.snowflake.com/en/user-guide/ui-snowsight/notebooks-in-workspaces/notebooks-in-workspaces-overview

  
  
#### Examples

* https://github.com/tspannhw/snowflake-distribution-insights-demo

