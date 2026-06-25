### Answers to Questions



#### IP Tools

* https://ipinfo.io/integrations/snowflake


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
  
* https://www.snowflake.com/en/blog/engineering/native-semantic-views-ai-bi/

* https://docs.snowflake.com/en/user-guide/views-semantic/editor

* https://docs.snowflake.com/en/user-guide/views-semantic/autopilot



#### Workspaces not Worksheets (SQL, Python, Jupyter Notebooks)

* https://docs.snowflake.com/en/user-guide/ui-workspaces-python

* https://docs.snowflake.com/en/user-guide/ui-snowsight/notebooks-in-workspaces/notebooks-in-workspaces-overview

* https://docs.snowflake.com/en/developer-guide/streamlit/streamlit-in-workspaces/streamlit-in-workspaces-overview
  
* https://docs.snowflake.com/en/user-guide/ui-snowsight/workspaces-git




#### DEMO SQL

````

USE SCHEMA CTF.PUBLIC;

SELECT * FROM VULNERABILITIES;



SELECT * FROM VULNERABILITIES WHERE TITLE ILIKE '%LOG4J%' AND STATUS = 'Open';




SELECT * FROM ACCESS_LOGS WHERE REQUEST_PATH ILIKE '%${jndi%';



SELECT ai.*
FROM (
    SELECT a.*, v.RESOURCE_EXTERNAL_ID, v.RESOURCE_HOSTNAME, v.RESOURCE_IP,
           v.TITLE, v.SEVERITY, v.STATUS AS VULN_STATUS
    FROM ACCESS_LOGS a
    JOIN VULNERABILITIES v
        ON a.BACKEND_IP = v.RESOURCE_IP
    WHERE LOWER(v.TITLE) LIKE '%log4j%'
      AND a.REQUEST_PATH ILIKE '%${jndi%'
) attacks
JOIN ASSET_INVENTORY ai
    ON attacks.RESOURCE_EXTERNAL_ID = ai.ID;


````



  
#### Examples

* https://github.com/tspannhw/snowflake-distribution-insights-demo


#### Alerts

* https://docs.snowflake.com/en/user-guide/alerts
* https://docs.snowflake.com/en/user-guide/notifications/about-notifications
  

#### Performance Enhancements

* https://docs.snowflake.com/en/user-guide/warehouses-gen2
* https://docs.snowflake.com/en/user-guide/warehouses-adaptive
* https://docs.snowflake.com/en/user-guide/query-acceleration-service
* https://docs.snowflake.com/en/user-guide/warehouses-considerations
* https://docs.snowflake.com/en/guides-overview-performance
* https://docs.snowflake.com/en/user-guide/snowflake-optima
* https://docs.snowflake.com/en/user-guide/performance-explorer
* https://www.snowflake.com/en/product/use-cases/well-architected-framework/


#### References


* https://github.com/tspannhw/AllDataAndAIWeekly/blob/main/2026/247-22June2026.md
* https://www.snowflake.com/en/developers/guides/coco-foundations/
* https://docs.snowflake.com/en/user-guide/trust-center/overview
* https://docs.snowflake.com/en/user-guide/cortex-code/data-platforms
* https://docs.snowflake.com/en/user-guide/cortex-code/cortex-code-mcp
* https://docs.snowflake.com/en/user-guide/cortex-code/extensibility
* https://docs.snowflake.com/en/user-guide/cortex-code-agent-sdk/cortex-code-agent-sdk

  
