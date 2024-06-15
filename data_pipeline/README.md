# Data Pipeline

- ERP - Source (postgres)
	- pedidos
	- clientes	
- List of Values - Source (minio)	
	- sexo
- Data Ingestion (Airbyte)
- Destination (postgres) bronze
- dbt (transformation)
	- mapping
	- uppercase

### Repositórios

- https://github.com/acnaweb/database
- https://github.com/acnaweb/minio
- https://github.com/acnaweb/airbyte

### Datasets

- s3://marketmining-public/domain_sexo.csv
- s3://marketmining-public/mapping_rules.csv


## Referencias

https://reference.airbyte.com/reference/start
https://docs.airbyte.com/operator-guides/collecting-metrics