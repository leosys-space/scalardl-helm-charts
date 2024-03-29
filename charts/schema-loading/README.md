# schema-loading

A schema loading tool for Scalar DL.
Current chart version is `2.0.0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| schemaLoading.cassandraReplicationFactor | int | `3` | The replication factor value of the Cassandra schema. This is a Cassandra specific option. |
| schemaLoading.contactPoints | string | `"cassandra"` | The database contanct point such as a hostname of Cassandra or a URL of Cosmos DB account. |
| schemaLoading.contactPort | int | `9042` | The database port number. (Ignored if the database is `cosmos`.) |
| schemaLoading.cosmosBaseResourceUnit | int | `400` | The resource unit value of the Cosmos DB schema. This is a Cosmos DB specific option. |
| schemaLoading.database | string | `"cassandra"` | The database to which the schema is loaded. `cassandra` and `cosmos` are supported. |
| schemaLoading.dynamoBaseResourceUnit | int | `10` | The resource unit value of the DynamoDB schema. This is a DynamoDB specific option. |
| schemaLoading.existingSecret | string | `nil` | Name of existing secret to use for storing database username and password |
| schemaLoading.image.pullPolicy | string | `"IfNotPresent"` | Specify a imagePullPolicy |
| schemaLoading.image.repository | string | `"ghcr.io/scalar-labs/scalardl-schema-loader"` | Docker image |
| schemaLoading.image.version | string | `"3.0.0"` | Docker tag |
| schemaLoading.imagePullSecrets | list | `[{"name":"reg-docker-secrets"}]` | Optionally specify an array of imagePullSecrets. Secrets must be manually created in the namespace. |
| schemaLoading.password | string | `"cassandra"` | The password of the database. For Cosmos DB, please specify a key here. |
| schemaLoading.username | string | `"cassandra"` | The username of the database. (Ignored if the database is `cosmos`.) |
