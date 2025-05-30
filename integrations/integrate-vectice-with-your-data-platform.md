# Integrate Vectice with your data platform

### How to integrate Vectice with Data Platforms

Here are some examples of how to connect Vectice with the following Data Platforms. For more details, check our [API cheatsheets](../log-and-manage-assets-with-vectice-api/api-cheatsheets/) for instructions on logging assets through these integrations.

```python
from vectice import DatabricksTableResource

db_resource = DatabricksTableResource(
    spark_client=spark,
    paths="my_table",
)
```
```python
from vectice import BigQueryResource

bq_resource = BigQueryResource(
    paths="bigquery-public-data.stackoverflow.posts_questions",
)
```

```python
from vectice import GCSResource

gcs_resource = GCSResource(
    uris="gs://<bucket_name>/<file_path_inside_bucket>",
)

```python
from vectice import S3Resource

s3_resource = S3Resource(
    uris="s3://<bucket_name>/<file_path_inside_bucket>",
)
```

```python
from vectice import SnowflakeResource, Dataset

connection_parameters = {
    ...
}
new_session = Session.builder.configs(connection_parameters).create()

sf_resource = SnowflakeResource(
    snowflake_client=new_session,
    paths="SNOWFLAKE_SAMPLE_DATA.TPCH_SF10.PART",
)
```

```python
from vectice import SparkTableResource

db_resource = SparkTableResource(
    spark_client=spark,
    paths="my_table",
)
```

To learn more about the code wrappers, visit our [API reference docs](https://api-docs.vectice.com/reference/vectice/).
