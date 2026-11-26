## Appendix: Answer key and explanations
 
### Answer grid (quick marking)
 
| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|
| 1 | B | 31 | C | 61 | A | 91 | A | 121 | A |
| 2 | D | 32 | C | 62 | B | 92 | B | 122 | B |
| 3 | B | 33 | A | 63 | D | 93 | B | 123 | D |
| 4 | C | 34 | D | 64 | D | 94 | A | 124 | B |
| 5 | C | 35 | D | 65 | A | 95 | B | 125 | D |
| 6 | A | 36 | C | 66 | A | 96 | D | 126 | A |
| 7 | A | 37 | B | 67 | A | 97 | A | 127 | D |
| 8 | D | 38 | C | 68 | B | 98 | B | 128 | D |
| 9 | A | 39 | B | 69 | A | 99 | C | 129 | D |
| 10 | B | 40 | B | 70 | D | 100 | B | 130 | A |
| 11 | B | 41 | D | 71 | C | 101 | B | 131 | B |
| 12 | B | 42 | D | 72 | D | 102 | A | 132 | A |
| 13 | C | 43 | D | 73 | A | 103 | D | 133 | D |
| 14 | A | 44 | C | 74 | C | 104 | D | 134 | C |
| 15 | B | 45 | C | 75 | A | 105 | A | 135 | C |
| 16 | B | 46 | A | 76 | B | 106 | A | 136 | B |
| 17 | C | 47 | C | 77 | B | 107 | C | 137 | C |
| 18 | D | 48 | B | 78 | D | 108 | C | 138 | D |
| 19 | A | 49 | B | 79 | C | 109 | A | 139 | A |
| 20 | C | 50 | D | 80 | D | 110 | A | 140 | A |
| 21 | D | 51 | C | 81 | C | 111 | A | 141 | B |
| 22 | A | 52 | B | 82 | B | 112 | D | 142 | B |
| 23 | D | 53 | C | 83 | A | 113 | A | 143 | D |
| 24 | C | 54 | D | 84 | C | 114 | A | 144 | D |
| 25 | D | 55 | A | 85 | C | 115 | A | 145 | C |
| 26 | B | 56 | C | 86 | D | 116 | C | 146 | B |
| 27 | C | 57 | B | 87 | B | 117 | A | 147 | C |
| 28 | B | 58 | C | 88 | B | 118 | C | 148 | C |
| 29 | C | 59 | D | 89 | C | 119 | D | 149 | A |
| 30 | B | 60 | D | 90 | B | 120 | D | 150 | A |
 
### Score sheet
 
| Domain | Questions | Your score |
|---|---|---|
| Snowflake AI Data Cloud Features and Architecture | Q1–Q47 | ___ / 47 |
| Account Management and Data Governance | Q48–Q77 | ___ / 30 |
| Data Loading, Unloading, and Connectivity | Q78–Q104 | ___ / 27 |
| Performance Optimization, Querying, and Transformation | Q105–Q135 | ___ / 31 |
| Data Collaboration | Q136–Q150 | ___ / 15 |
| **Total** | 150 | ___ / 150 |
 
### Domain 1: Snowflake AI Data Cloud Features and Architecture
 
| Q | Answer | Explanation |
|---|---|---|
| 1 | **B** | The cloud services layer coordinates authentication, metadata, access control, and optimization. |
| 2 | **D** | Warehouses are independent compute clusters that read the same central storage. |
| 3 | **B** | Virtual warehouses form the compute layer that executes queries. |
| 4 | **C** | Multi-cluster warehouses require Enterprise Edition or higher. |
| 5 | **C** | PHI support requires Business Critical Edition or higher. |
| 6 | **A** | Dynamic tables are in all editions. The other three require Enterprise or higher. |
| 7 | **A** | VPS is the most isolated edition. |
| 8 | **D** | Snowsight is the browser-based user interface. |
| 9 | **A** | Snowflake CLI is the developer-focused command-line tool invoked with `snow`. |
| 10 | **B** | IDE integrations such as the VS Code extension support development in the editor. |
| 11 | **B** | Organizations contain accounts, which contain databases, schemas, and schema objects. |
| 12 | **B** | Warehouses belong to the account. Stages, file formats, and sequences live in schemas. |
| 13 | **C** | For session parameters, session overrides user, which overrides account. |
| 14 | **A** | A value set explicitly on a lower-level object overrides the inherited value. |
| 15 | **B** | SET creates a SQL session variable, referenced with a $ prefix. |
| 16 | **B** | CURRENT_ROLE() is a context function. |
| 17 | **C** | Micro-partitioning is automatic, columnar, and the files are immutable. |
| 18 | **D** | Each micro-partition holds about 50-500 MB of uncompressed data. |
| 19 | **A** | Micro-partitions are immutable. Older versions support Time Travel and Fail-safe. |
| 20 | **C** | This is query pruning. |
| 21 | **D** | Clustering maintenance costs credits, so it pays off mainly on large, selectively queried tables. |
| 22 | **A** | Lower depth means less overlap among micro-partitions. |
| 23 | **D** | Temporary tables are dropped when the session ends and are not visible to other sessions. |
| 24 | **C** | Transient tables persist until dropped and have no Fail-safe period. |
| 25 | **D** | Permanent is the default. |
| 26 | **B** | External table data stays in external storage and cannot be modified with DML. |
| 27 | **C** | Iceberg is an open table format that lets data be used in a lakehouse design. |
| 28 | **B** | A dynamic table is defined by a query and a TARGET_LAG. |
| 29 | **C** | Standard views hold no data. |
| 30 | **B** | Joins are not supported in a materialized view definition. |
| 31 | **C** | Secure views protect definition and underlying data, sometimes at the cost of performance. |
| 32 | **C** | XS=1, S=2, M=4, L=8. |
| 33 | **A** | Scaling up gives each query more resources. Scaling out addresses concurrency. |
| 34 | **D** | Scaling out adds clusters to handle concurrency. |
| 35 | **D** | Equal values above 1 start all clusters whenever the warehouse runs. |
| 36 | **C** | Economy conserves credits. Standard favours starting clusters to minimize queuing. |
| 37 | **B** | AUTO_SUSPEND is expressed in seconds. |
| 38 | **C** | Resizing does not affect statements already executing. |
| 39 | **B** | Snowpark-optimized warehouses provide much more memory per node. |
| 40 | **B** | Gen2 is a newer standard warehouse generation, with its own credit rates. |
| 41 | **D** | Separate warehouses isolate compute while sharing the same data. |
| 42 | **D** | Notebooks provide a cell-based development experience. |
| 43 | **D** | Streamlit in Snowflake hosts Python apps next to the data. |
| 44 | **C** | Snowpark offers DataFrame-style programming with execution in Snowflake. |
| 45 | **C** | Cortex Analyst converts natural language to SQL using semantic definitions. |
| 46 | **A** | Cortex Search is a managed search service for unstructured text. Search optimization is for table lookups. |
| 47 | **C** | Snowflake ML includes tooling such as a model registry and feature store. |
 
### Domain 2: Account Management and Data Governance
 
| Q | Answer | Explanation |
|---|---|---|
| 48 | **B** | RBAC assigns privileges to roles. Snowflake also offers user-based grants, but roles are the core model. |
| 49 | **B** | Under DAC, the owner controls grants on the object. |
| 50 | **D** | USERADMIN is dedicated to user and role management. |
| 51 | **C** | SECURITYADMIN can manage grants globally. |
| 52 | **B** | SYSADMIN has privileges to create warehouses and databases. |
| 53 | **C** | PUBLIC is the baseline role for everyone. |
| 54 | **D** | Rolling up to SYSADMIN lets system administrators manage the objects owned by custom roles. |
| 55 | **A** | ACCOUNTADMIN is powerful but not a superuser that ignores privileges. |
| 56 | **C** | Database roles are granted to account roles or other database roles. |
| 57 | **B** | Object creation is still governed by the primary role. |
| 58 | **C** | Network policies allow or block network origins. |
| 59 | **D** | Network policies take precedence over authentication policies. |
| 60 | **D** | Service users need strong authentication that requires no human interaction. |
| 61 | **A** | Federation delegates authentication to an identity provider, commonly using SAML 2.0. |
| 62 | **B** | Snowflake is deprecating single-factor password logins in a phased rollout. |
| 63 | **D** | The organization name plus account name is the preferred identifier. |
| 64 | **D** | Event tables store logs, traces, and related telemetry. |
| 65 | **A** | Masking policies are applied at query runtime. |
| 66 | **A** | Row access policies filter which rows are returned. |
| 67 | **A** | Tags support governance, tracking, and cost attribution. |
| 68 | **B** | Direct assignment wins over tag-based assignment. |
| 69 | **A** | Aggregation policies protect individuals by enforcing minimum group sizes. |
| 70 | **D** | The Trust Center runs scanner packages to identify security risks. |
| 71 | **C** | It requires Business Critical Edition or higher and gives the customer control over one key. |
| 72 | **D** | Alerts combine a condition, an action, and a schedule or trigger. |
| 73 | **A** | Lineage shows upstream and downstream relationships. |
| 74 | **C** | Suspend lets running statements finish. Suspend immediately cancels them. |
| 75 | **A** | 4 credits per hour x 3 clusters x 2 hours = 24. |
| 76 | **B** | Only usage above 10% of daily warehouse credits is billed: 13 - 10 = 3. |
| 77 | **B** | ACCOUNT_USAGE retains history for up to a year, with some latency. |
 
### Domain 3: Data Loading, Unloading, and Connectivity
 
| Q | Answer | Explanation |
|---|---|---|
| 78 | **D** | @~ is the user stage, @%name a table stage, and @name a named stage. |
| 79 | **C** | Git integration syncs a remote repository into a Git repository stage in Snowflake. |
| 80 | **D** | PUT uploads local files to internal stages. |
| 81 | **C** | GET is the reverse of PUT. |
| 82 | **B** | AUTO_COMPRESS is TRUE by default. |
| 83 | **A** | SNOWFLAKE_SSE selects server-side encryption, which is often needed for unstructured file access. |
| 84 | **C** | Unloading supports delimited text (CSV), JSON, and Parquet. |
| 85 | **C** | File formats centralize parsing options. |
| 86 | **D** | Files of this size allow efficient parallel loading. |
| 87 | **B** | STRIP_OUTER_ARRAY removes the enclosing brackets. |
| 88 | **B** | Bulk COPY aborts by default. |
| 89 | **C** | Snowpipe skips a file containing errors by default. |
| 90 | **B** | VALIDATION_MODE returns results instead of loading. It does not support COPY statements that transform data. |
| 91 | **A** | COPY uses 64-day load metadata to avoid reloading files. |
| 92 | **B** | FORCE ignores load history and can create duplicates. |
| 93 | **B** | PURGE cleans up successfully loaded files. |
| 94 | **A** | SINGLE defaults to FALSE to allow parallel unloading. |
| 95 | **B** | Directory tables catalogue staged files. |
| 96 | **D** | Snowpipe is serverless. |
| 97 | **A** | AUTO_INGEST uses event notifications; applications can instead call the REST API. |
| 98 | **B** | Snowpipe Streaming writes rows directly into tables. |
| 99 | **C** | A stream exposes change data from an offset. |
| 100 | **B** | Queries alone do not consume a stream. |
| 101 | **B** | The function returns TRUE when the stream has change records. |
| 102 | **A** | Tasks are created in a suspended state. |
| 103 | **D** | Target lag is a best-effort freshness target, not a fixed schedule. |
| 104 | **D** | A storage integration holds a cloud identity configuration for external storage access. |
 
### Domain 4: Performance Optimization, Querying, and Transformation
 
| Q | Answer | Explanation |
|---|---|---|
| 105 | **A** | Query Profile breaks down execution by operator. |
| 106 | **A** | Spilling indicates the operation does not fit in memory and local disk. |
| 107 | **C** | Remote storage is much slower than local disk. |
| 108 | **C** | Few partitions were eliminated. |
| 109 | **A** | Check join keys and duplicates. |
| 110 | **A** | Queuing from overload means the warehouse cannot run all queries at once. |
| 111 | **A** | Query attribution history assigns compute credits to queries. |
| 112 | **D** | QUERY_HISTORY records query-level metrics. |
| 113 | **A** | Grouping similar workloads makes sizing and cost control easier. |
| 114 | **A** | It limits execution time. |
| 115 | **A** | QAS offloads parts of large scan work to serverless compute. |
| 116 | **C** | Search optimization targets needle-in-a-haystack queries. |
| 117 | **A** | The search access path tracks where values may be found among micro-partitions. |
| 118 | **C** | Materialized views store precomputed results. |
| 119 | **D** | Reclustering rewrites micro-partitions. |
| 120 | **D** | Choose keys that improve pruning, usually only a few columns. |
| 121 | **A** | Results persist for 24 hours. |
| 122 | **B** | Each reuse resets the 24-hour window, up to 31 days. |
| 123 | **D** | Reuse also requires appropriate privileges and other conditions. |
| 124 | **B** | Warehouses cache table data they read. |
| 125 | **D** | Weigh this when setting auto-suspend. |
| 126 | **A** | Row counts are maintained in metadata. |
| 127 | **D** | Use a colon for the first level, dots for nested levels, and :: to cast. |
| 128 | **D** | FLATTEN is commonly used with LATERAL. |
| 129 | **D** | PARSE_JSON parses text into VARIANT. |
| 130 | **A** | QUALIFY is evaluated after window functions. |
| 131 | **B** | DENSE_RANK produces 1, 1, 2. RANK produces 1, 1, 3. |
| 132 | **A** | COUNT of a column ignores NULLs. |
| 133 | **D** | It uses HyperLogLog estimation. |
| 134 | **C** | UNION performs extra deduplication. |
| 135 | **C** | Pre-signed URLs give temporary access to unstructured files. |
 
### Domain 5: Data Collaboration
 
| Q | Answer | Explanation |
|---|---|---|
| 136 | **B** | Storage grows only as the source or clone changes. |
| 137 | **C** | Database and share replication work in all editions; failover groups require Business Critical or higher. |
| 138 | **D** | The default is one day. |
| 139 | **A** | Enterprise and higher allow up to 90 days. |
| 140 | **A** | Fail-safe is a non-configurable 7-day period after Time Travel. |
| 141 | **B** | Fail-safe is not directly queryable by customers. |
| 142 | **B** | UNDROP restores dropped tables, schemas, and databases. |
| 143 | **D** | BEFORE excludes the changes made by the specified statement. |
| 144 | **D** | Consumers use their own warehouses. |
| 145 | **C** | Sharing relies on metadata and services; no data is transferred. |
| 146 | **B** | Reader accounts are created and managed by the provider. |
| 147 | **C** | A reader account consumes data only from the provider that created it. |
| 148 | **C** | Listings extend Secure Data Sharing. |
| 149 | **A** | Clean rooms support privacy-preserving collaboration. |
| 150 | **A** | Native Apps are installed and run in the consumer's account. |
