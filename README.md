# SnowPro Core (COF-C03): Study Guide and 150-Question Practice Quiz
 
*Prepared 26 November 2026.*
 
**Contents**
 
- [Part 1: Exam snapshot](#part-1-exam-snapshot)
- [Part 2: Study outline, in order](#part-2-study-outline-in-order)
- [Part 3: Quick-reference sheet](#part-3-quick-reference-sheet)
- [Part 4: Practice quiz (150 questions)](#part-4-practice-quiz-150-questions)
- [Appendix: Answer key and explanations](#appendix-answer-key-and-explanations)
---
 
## Part 1: Exam snapshot
 
| Item | Detail |
|---|---|
| Exam code | COF-C03 (launched 16 February 2026, replaces COF-C02) |
| Questions | 100, multiple choice and multiple select |
| Time | 115 minutes |
| Passing score | 750 on a 0–1000 scale |
| Fee | Mostly reported as US$175 (one source differs, so confirm at registration) |
| Recommended experience | 6 or more months using Snowflake |
 
| Domain | Weight | Questions in this quiz |
|---|---|---|
| 1. Snowflake AI Data Cloud Features and Architecture | 31% | 47 (Q1–Q47) |
| 2. Account Management and Data Governance | 20% | 30 (Q48–Q77) |
| 3. Data Loading, Unloading, and Connectivity | 18% | 27 (Q78–Q104) |
| 4. Performance Optimization, Querying, and Transformation | 21% | 31 (Q105–Q135) |
| 5. Data Collaboration | 10% | 15 (Q136–Q150) |
 
> **Verify before you book.** The official exam page could not be opened while this guide was prepared. The format, weights, and objective list come from third-party reproductions of the exam guide. Download the current guide from the [official COF-C03 page](https://learn.snowflake.com/en/certifications/snowpro-core-c03/) and compare it with Part 2.
 
---
 
## Part 2: Study outline, in order
 
The order builds each topic on the one before it. It differs slightly from the exam numbering: storage and object concepts come before warehouses. The suggested plan is about 6 weeks at 1–2 hours per day.
 
**Reference legend:** links without a mark appeared in documentation searches done for this guide. Links marked † are from general knowledge of the documentation site and were not checked, so search the page title if one has moved.

### Step 0: Set up (1 day)
 
- [ ] Download the official exam guide
- [ ] Create a Snowflake trial account (Enterprise edition lets you practise more features)
- [ ] Create an X-Small warehouse with a short auto-suspend, plus a resource monitor to protect trial credits
References: [Exam page](https://learn.snowflake.com/en/certifications/snowpro-core-c03/) · [Official practice exams](https://learn.snowflake.com/en/certifications/snowpro-practice-exams/) · [Essentials for SnowPro Core course track](https://www.snowflake.com/en/developers/northstar/)
 
### Step 1: Architecture and editions (Week 1) · Objectives 1.1, 1.2
 
- [ ] Three layers: database storage, compute, cloud services. Know which task belongs to which
- [ ] Multi-cluster, shared-data design and separation of storage from compute
- [ ] Editions: Standard, Enterprise, Business Critical, Virtual Private Snowflake (VPS). Memorise which features start at which edition
- [ ] Interfaces: Snowsight, Snowflake CLI, IDE integrations such as VS Code
References:
- [Key concepts and architecture](https://docs.snowflake.com/en/user-guide/intro-key-concepts)
- [Snowflake editions](https://docs.snowflake.com/en/user-guide/intro-editions)
- [Overview of key features](https://docs.snowflake.com/en/user-guide/intro-supported-features)
- [Snowsight](https://docs.snowflake.com/en/user-guide/ui-snowsight) † · [Snowflake CLI](https://docs.snowflake.com/en/developer-guide/snowflake-cli/index) † · [VS Code extension](https://docs.snowflake.com/en/user-guide/vscode-ext) †
### Step 2: Storage concepts and object model (Week 1) · Objectives 1.3, 1.5
 
- [ ] Micro-partitions: columnar, immutable, 50–500 MB uncompressed, metadata used for pruning
- [ ] Natural clustering, clustering depth, clustering keys
- [ ] Table types: permanent, transient, temporary, external, Apache Iceberg, dynamic
- [ ] View types: standard, materialized, secure
- [ ] Hierarchy: organization → account → database → schema → schema objects
- [ ] Account-level objects compared with schema-level objects
- [ ] Parameter hierarchy and precedence; session and context variables
References:
- [Micro-partitions and data clustering](https://docs.snowflake.com/en/user-guide/tables-clustering-micropartitions) †
- [Temporary and transient tables](https://docs.snowflake.com/en/user-guide/tables-temp-transient)
- [External tables](https://docs.snowflake.com/en/user-guide/tables-external-intro)
- [Views](https://docs.snowflake.com/en/user-guide/views-introduction) † · [Materialized views](https://docs.snowflake.com/en/user-guide/views-materialized) †
- [Parameters](https://docs.snowflake.com/en/sql-reference/parameters)
**Lab:** create one table of each of the permanent, transient, and temporary types, then compare them with `SHOW TABLES`.
 
### Step 3: Virtual warehouses (Week 2) · Objective 1.4
 
- [ ] Sizes and credits per hour (Gen1); per-second billing with a 60-second minimum
- [ ] Standard (Gen1 and Gen2) and Snowpark-optimized warehouses
- [ ] Scale **up/down** (size) for complex queries; scale **out/in** (clusters) for concurrency
- [ ] Multi-cluster modes (Maximized, Auto-scale) and scaling policies (Standard, Economy)
- [ ] Auto-suspend, auto-resume, workload isolation by team and use case
References:
- [Overview of warehouses](https://docs.snowflake.com/en/user-guide/warehouses-overview)
- [Warehouse considerations](https://docs.snowflake.com/en/user-guide/warehouses-considerations)
- [Multi-cluster warehouses](https://docs.snowflake.com/en/user-guide/warehouses-multicluster)
- [CREATE WAREHOUSE](https://docs.snowflake.com/en/sql-reference/sql/create-warehouse)
- [Gen2 warehouses](https://docs.snowflake.com/en/user-guide/warehouses-gen2) † · [Snowpark-optimized warehouses](https://docs.snowflake.com/en/user-guide/warehouses-snowpark-optimized) †
### Step 4: AI/ML and application development (Week 2) · Objective 1.6
 
Focus on what each feature is for. Third-party guidance says deep Cortex function syntax is not required.
 
- [ ] Snowflake Notebooks, Streamlit in Snowflake, Snowpark
- [ ] Cortex AI Functions, Cortex Search, Cortex Analyst
- [ ] Snowflake ML
References:
- [Notebooks](https://docs.snowflake.com/en/user-guide/ui-snowsight/notebooks) † · [Streamlit in Snowflake](https://docs.snowflake.com/en/developer-guide/streamlit/about-streamlit) † · [Snowpark](https://docs.snowflake.com/en/developer-guide/snowpark/index) †
- [Cortex AI Functions](https://docs.snowflake.com/en/user-guide/snowflake-cortex/aisql) † · [Cortex Search](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-search/cortex-search-overview) † · [Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst) †
- [Cortex Agents](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-agents) (useful context on how Analyst and Search differ)
- [Snowflake ML](https://docs.snowflake.com/en/developer-guide/snowflake-ml/overview) †
### Step 5: Security and access control (Week 3) · Objective 2.1
 
- [ ] Role-based access control (RBAC) and discretionary access control (DAC); securable object hierarchy
- [ ] System roles: ORGADMIN, ACCOUNTADMIN, SECURITYADMIN, USERADMIN, SYSADMIN, PUBLIC
- [ ] Account roles, database roles, custom and functional roles, secondary roles
- [ ] Authentication: MFA, SSO/federation (SAML), OAuth, key-pair
- [ ] Network policies, authentication policies, account identifiers
- [ ] Logging and tracing with event tables
References:
- [Access control overview](https://docs.snowflake.com/en/user-guide/security-access-control-overview)
- [Access control best practices](https://docs.snowflake.com/en/user-guide/security-access-control-considerations)
- [Configuring access control](https://docs.snowflake.com/en/user-guide/security-access-control-configure)
- [Network policies](https://docs.snowflake.com/en/user-guide/network-policies)
- [Authentication policies](https://docs.snowflake.com/en/user-guide/authentication-policies)
- [Deprecation of single-factor password sign-ins](https://docs.snowflake.com/en/user-guide/security-mfa-rollout)
- [Key-pair authentication](https://docs.snowflake.com/en/user-guide/key-pair-auth) † · [Federated authentication](https://docs.snowflake.com/en/user-guide/admin-security-fed-auth-overview) † · [Account identifiers](https://docs.snowflake.com/en/user-guide/admin-account-identifier) †
- [Logging and tracing](https://docs.snowflake.com/en/developer-guide/logging-tracing/logging-tracing-overview) †
**Lab:** build a small role hierarchy, grant it to SYSADMIN, and test access with `USE ROLE`.
 
### Step 6: Data governance (Week 3) · Objective 2.2
 
- [ ] Column-level security (masking policies) and row-level security (row access policies)
- [ ] Object tagging and tag-based masking; privacy-related policies (aggregation, projection, differential privacy)
- [ ] Trust Center, encryption and key management, Tri-Secret Secure
- [ ] Alerts, notifications, data lineage
- [ ] Replication and failover, including edition requirements
References:
- [Column-level security](https://docs.snowflake.com/en/user-guide/security-column-intro) · [Tag-based masking](https://docs.snowflake.com/en/user-guide/tag-based-masking-policies)
- [Row access policies](https://docs.snowflake.com/en/user-guide/security-row-intro) † · [Object tagging](https://docs.snowflake.com/en/user-guide/object-tagging) †
- [Using the Trust Center](https://docs.snowflake.com/en/user-guide/trust-center/using-the-trust-center)
- [Encryption key management](https://docs.snowflake.com/en/user-guide/security-encryption-manage) † · [Alerts](https://docs.snowflake.com/en/user-guide/alerts) † · [Data lineage](https://docs.snowflake.com/en/user-guide/ui-snowsight-lineage) †
- [Replication and failover](https://docs.snowflake.com/en/user-guide/account-replication-intro)
### Step 7: Monitoring and cost management (Week 3) · Objective 2.3
 
- [ ] Compute, storage, serverless, and cloud services costs
- [ ] The 10% cloud services billing adjustment
- [ ] Resource monitors (warehouses) compared with budgets (broader, including serverless)
- [ ] `ACCOUNT_USAGE` compared with `INFORMATION_SCHEMA`: latency, retention, dropped objects
- [ ] Practise credit calculations
References:
- [Understanding overall cost](https://docs.snowflake.com/en/user-guide/cost-understanding-overall) · [Compute cost](https://docs.snowflake.com/en/user-guide/cost-understanding-compute) · [Storage cost](https://docs.snowflake.com/en/user-guide/cost-understanding-data-storage)
- [Resource monitors](https://docs.snowflake.com/en/user-guide/resource-monitors) · [Controlling cost](https://docs.snowflake.com/en/user-guide/cost-controlling)
- [Exploring compute cost](https://docs.snowflake.com/en/user-guide/cost-exploring-compute) · [Account Usage](https://docs.snowflake.com/en/sql-reference/account-usage)
### Step 8: Loading and unloading (Week 4) · Objective 3.1
 
- [ ] Stages: user, table, named internal, external; server-side encryption
- [ ] File formats; supported formats for loading compared with unloading
- [ ] `PUT`, `GET`, `LIST`, `REMOVE`; `COPY INTO <table>` and `COPY INTO <location>`
- [ ] `ON_ERROR`, `VALIDATION_MODE`, `VALIDATE`, `FORCE`, `PURGE`, load metadata
- [ ] Directory tables; file sizing best practice
References:
- [Overview of data loading](https://docs.snowflake.com/en/user-guide/data-load-overview) · [Loading considerations](https://docs.snowflake.com/en/user-guide/data-load-considerations-load)
- [COPY INTO table](https://docs.snowflake.com/en/sql-reference/sql/copy-into-table) · [COPY INTO location](https://docs.snowflake.com/en/sql-reference/sql/copy-into-location)
- [Transforming data during a load](https://docs.snowflake.com/en/user-guide/data-load-transform)
- [Directory tables](https://docs.snowflake.com/en/user-guide/data-load-dirtables) † · [Data unloading](https://docs.snowflake.com/en/user-guide/data-unload-overview) †
**Lab:** upload a CSV with deliberate errors, run `VALIDATION_MODE`, load it with different `ON_ERROR` settings, then unload to Parquet.
 
### Step 9: Automated ingestion and connectivity (Week 4) · Objectives 3.2, 3.3
 
- [ ] Snowpipe (auto-ingest and REST API) compared with bulk `COPY` and Snowpipe Streaming
- [ ] Streams: types, metadata columns, offsets, staleness
- [ ] Tasks: schedules, task graphs, serverless or warehouse compute
- [ ] Dynamic tables and target lag
- [ ] Drivers, connectors, storage integration, API integration, Git integration
- [ ] Openflow was listed as not tested until globally generally available, so check the current guide
References:
- [Snowpipe](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-intro) · [Auto-ingest](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-auto) · [REST API](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-rest-overview) · [Costs](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-billing)
- [Snowpipe Streaming](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-streaming-overview)
- [Streams](https://docs.snowflake.com/en/user-guide/streams-intro) · [Tasks](https://docs.snowflake.com/en/user-guide/tasks-intro) †
- [Dynamic table target lag](https://docs.snowflake.com/en/user-guide/dynamic-tables/target-lag) · [Dynamic tables, streams and tasks, or materialized views](https://docs.snowflake.com/en/user-guide/dynamic-tables/decision-guide)
- [Drivers](https://docs.snowflake.com/en/developer-guide/drivers) † · [Storage integration for S3](https://docs.snowflake.com/en/user-guide/data-load-s3-config-storage-integration) † · [Git integration](https://docs.snowflake.com/en/developer-guide/git/git-overview) †
### Step 10: Performance and caching (Week 5) · Objectives 4.1–4.3
 
- [ ] Query Profile and Query Insights: spilling, pruning, exploding joins, queuing
- [ ] Query history and query attribution views
- [ ] Query acceleration, search optimization, clustering keys, materialized views: when to use each
- [ ] Result cache, metadata cache, warehouse cache
- [ ] Workload management: group similar workloads
 
References:
- [Optimizing query performance](https://docs.snowflake.com/en/user-guide/performance-query-options) · [Optimizing storage for performance](https://docs.snowflake.com/en/user-guide/performance-query-storage)
- [Query Profile](https://docs.snowflake.com/en/user-guide/ui-query-profile) †
- [Query Acceleration Service](https://docs.snowflake.com/en/user-guide/query-acceleration-service) · [Search optimization](https://docs.snowflake.com/en/user-guide/search-optimization-service) · [Clustering keys](https://docs.snowflake.com/en/user-guide/tables-clustering-keys) †
- [Persisted query results](https://docs.snowflake.com/en/user-guide/querying-persisted-results) · [RESULT_SCAN](https://docs.snowflake.com/en/sql-reference/functions/result_scan)
**Lab:** run a query on `SNOWFLAKE_SAMPLE_DATA` twice, compare the profiles, then set `USE_CACHED_RESULT = FALSE` and run it again.
 
### Step 11: Querying and transformation (Week 5) · Objective 4.4
 
- [ ] Structured, semi-structured (`VARIANT`, `FLATTEN`), and unstructured data
- [ ] Aggregate and window functions, `QUALIFY`
- [ ] SQL habits that improve performance
- [ ] UDFs and stored procedures
References:
- [Querying semi-structured data](https://docs.snowflake.com/en/user-guide/querying-semistructured) † · [FLATTEN](https://docs.snowflake.com/en/sql-reference/functions/flatten) †
- [Window functions](https://docs.snowflake.com/en/user-guide/functions-window-using) †
- [Unstructured data](https://docs.snowflake.com/en/user-guide/unstructured-intro)
### Step 12: Data protection and collaboration (Week 6) · Objectives 5.1–5.3
 
- [ ] Time Travel, Fail-safe, `UNDROP`, zero-copy cloning
- [ ] Replication and failover
- [ ] Secure Data Sharing: providers, consumers, reader accounts, direct shares, resharing
- [ ] Data clean rooms
- [ ] Marketplace, public and private listings, Native Apps
References:
- [Time Travel](https://docs.snowflake.com/en/user-guide/data-time-travel) † · [Fail-safe](https://docs.snowflake.com/en/user-guide/data-failsafe) † · [Cloning](https://docs.snowflake.com/en/user-guide/object-clone) †
- [Storage costs for Time Travel and Fail-safe](https://docs.snowflake.com/en/user-guide/data-cdp-storage-costs)
- [Secure Data Sharing](https://docs.snowflake.com/en/user-guide/data-sharing-intro) · [Create shares](https://docs.snowflake.com/en/user-guide/data-sharing-provider) · [Consume shared data](https://docs.snowflake.com/en/user-guide/data-share-consumers) · [Reader accounts](https://docs.snowflake.com/en/user-guide/data-sharing-reader-create)
- [Listings](https://docs.snowflake.com/en/collaboration/collaboration-listings-about) · [Resharing](https://docs.snowflake.com/en/collaboration/resharing-as-resharer)
- [Data clean rooms](https://docs.snowflake.com/en/user-guide/cleanrooms/introduction) † · [Native Apps](https://docs.snowflake.com/en/developer-guide/native-apps/native-apps-about) †
> Resharing rules are changing. A 2026 behaviour change (listed as pending when checked) lets consumers reshare direct-share data within their own organization. See the [release note](https://docs.snowflake.com/en/release-notes/bcr-bundles/2026_06/bcr-2364).
### Step 0: Set up (1 day)
 
- [ ] Download the official exam guide
- [ ] Create a Snowflake trial account (Enterprise edition lets you practise more features)
- [ ] Create an X-Small warehouse with a short auto-suspend, plus a resource monitor to protect trial credits
References: [Exam page](https://learn.snowflake.com/en/certifications/snowpro-core-c03/) · [Official practice exams](https://learn.snowflake.com/en/certifications/snowpro-practice-exams/) · [Essentials for SnowPro Core course track](https://www.snowflake.com/en/developers/northstar/)
 
### Step 1: Architecture and editions (Week 1) · Objectives 1.1, 1.2
 
- [ ] Three layers: database storage, compute, cloud services. Know which task belongs to which
- [ ] Multi-cluster, shared-data design and separation of storage from compute
- [ ] Editions: Standard, Enterprise, Business Critical, Virtual Private Snowflake (VPS). Memorise which features start at which edition
- [ ] Interfaces: Snowsight, Snowflake CLI, IDE integrations such as VS Code
References:
- [Key concepts and architecture](https://docs.snowflake.com/en/user-guide/intro-key-concepts)
- [Snowflake editions](https://docs.snowflake.com/en/user-guide/intro-editions)
- [Overview of key features](https://docs.snowflake.com/en/user-guide/intro-supported-features)
- [Snowsight](https://docs.snowflake.com/en/user-guide/ui-snowsight) † · [Snowflake CLI](https://docs.snowflake.com/en/developer-guide/snowflake-cli/index) † · [VS Code extension](https://docs.snowflake.com/en/user-guide/vscode-ext) †
### Step 2: Storage concepts and object model (Week 1) · Objectives 1.3, 1.5
 
- [ ] Micro-partitions: columnar, immutable, 50–500 MB uncompressed, metadata used for pruning
- [ ] Natural clustering, clustering depth, clustering keys
- [ ] Table types: permanent, transient, temporary, external, Apache Iceberg, dynamic
- [ ] View types: standard, materialized, secure
- [ ] Hierarchy: organization → account → database → schema → schema objects
- [ ] Account-level objects compared with schema-level objects
- [ ] Parameter hierarchy and precedence; session and context variables
References:
- [Micro-partitions and data clustering](https://docs.snowflake.com/en/user-guide/tables-clustering-micropartitions) †
- [Temporary and transient tables](https://docs.snowflake.com/en/user-guide/tables-temp-transient)
- [External tables](https://docs.snowflake.com/en/user-guide/tables-external-intro)
- [Views](https://docs.snowflake.com/en/user-guide/views-introduction) † · [Materialized views](https://docs.snowflake.com/en/user-guide/views-materialized) †
- [Parameters](https://docs.snowflake.com/en/sql-reference/parameters)
**Lab:** create one table of each of the permanent, transient, and temporary types, then compare them with `SHOW TABLES`.
 
### Step 3: Virtual warehouses (Week 2) · Objective 1.4
 
- [ ] Sizes and credits per hour (Gen1); per-second billing with a 60-second minimum
- [ ] Standard (Gen1 and Gen2) and Snowpark-optimized warehouses
- [ ] Scale **up/down** (size) for complex queries; scale **out/in** (clusters) for concurrency
- [ ] Multi-cluster modes (Maximized, Auto-scale) and scaling policies (Standard, Economy)
- [ ] Auto-suspend, auto-resume, workload isolation by team and use case
References:
- [Overview of warehouses](https://docs.snowflake.com/en/user-guide/warehouses-overview)
- [Warehouse considerations](https://docs.snowflake.com/en/user-guide/warehouses-considerations)
- [Multi-cluster warehouses](https://docs.snowflake.com/en/user-guide/warehouses-multicluster)
- [CREATE WAREHOUSE](https://docs.snowflake.com/en/sql-reference/sql/create-warehouse)
- [Gen2 warehouses](https://docs.snowflake.com/en/user-guide/warehouses-gen2) † · [Snowpark-optimized warehouses](https://docs.snowflake.com/en/user-guide/warehouses-snowpark-optimized) †
### Step 4: AI/ML and application development (Week 2) · Objective 1.6
 
Focus on what each feature is for. Third-party guidance says deep Cortex function syntax is not required.
 
- [ ] Snowflake Notebooks, Streamlit in Snowflake, Snowpark
- [ ] Cortex AI Functions, Cortex Search, Cortex Analyst
- [ ] Snowflake ML
References:
- [Notebooks](https://docs.snowflake.com/en/user-guide/ui-snowsight/notebooks) † · [Streamlit in Snowflake](https://docs.snowflake.com/en/developer-guide/streamlit/about-streamlit) † · [Snowpark](https://docs.snowflake.com/en/developer-guide/snowpark/index) †
- [Cortex AI Functions](https://docs.snowflake.com/en/user-guide/snowflake-cortex/aisql) † · [Cortex Search](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-search/cortex-search-overview) † · [Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst) †
- [Cortex Agents](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-agents) (useful context on how Analyst and Search differ)
- [Snowflake ML](https://docs.snowflake.com/en/developer-guide/snowflake-ml/overview) †
### Step 5: Security and access control (Week 3) · Objective 2.1
 
- [ ] Role-based access control (RBAC) and discretionary access control (DAC); securable object hierarchy
- [ ] System roles: ORGADMIN, ACCOUNTADMIN, SECURITYADMIN, USERADMIN, SYSADMIN, PUBLIC
- [ ] Account roles, database roles, custom and functional roles, secondary roles
- [ ] Authentication: MFA, SSO/federation (SAML), OAuth, key-pair
- [ ] Network policies, authentication policies, account identifiers
- [ ] Logging and tracing with event tables
References:
- [Access control overview](https://docs.snowflake.com/en/user-guide/security-access-control-overview)
- [Access control best practices](https://docs.snowflake.com/en/user-guide/security-access-control-considerations)
- [Configuring access control](https://docs.snowflake.com/en/user-guide/security-access-control-configure)
- [Network policies](https://docs.snowflake.com/en/user-guide/network-policies)
- [Authentication policies](https://docs.snowflake.com/en/user-guide/authentication-policies)
- [Deprecation of single-factor password sign-ins](https://docs.snowflake.com/en/user-guide/security-mfa-rollout)
- [Key-pair authentication](https://docs.snowflake.com/en/user-guide/key-pair-auth) † · [Federated authentication](https://docs.snowflake.com/en/user-guide/admin-security-fed-auth-overview) † · [Account identifiers](https://docs.snowflake.com/en/user-guide/admin-account-identifier) †
- [Logging and tracing](https://docs.snowflake.com/en/developer-guide/logging-tracing/logging-tracing-overview) †
**Lab:** build a small role hierarchy, grant it to SYSADMIN, and test access with `USE ROLE`.
 
### Step 6: Data governance (Week 3) · Objective 2.2
 
- [ ] Column-level security (masking policies) and row-level security (row access policies)
- [ ] Object tagging and tag-based masking; privacy-related policies (aggregation, projection, differential privacy)
- [ ] Trust Center, encryption and key management, Tri-Secret Secure
- [ ] Alerts, notifications, data lineage
- [ ] Replication and failover, including edition requirements
References:
- [Column-level security](https://docs.snowflake.com/en/user-guide/security-column-intro) · [Tag-based masking](https://docs.snowflake.com/en/user-guide/tag-based-masking-policies)
- [Row access policies](https://docs.snowflake.com/en/user-guide/security-row-intro) † · [Object tagging](https://docs.snowflake.com/en/user-guide/object-tagging) †
- [Using the Trust Center](https://docs.snowflake.com/en/user-guide/trust-center/using-the-trust-center)
- [Encryption key management](https://docs.snowflake.com/en/user-guide/security-encryption-manage) † · [Alerts](https://docs.snowflake.com/en/user-guide/alerts) † · [Data lineage](https://docs.snowflake.com/en/user-guide/ui-snowsight-lineage) †
- [Replication and failover](https://docs.snowflake.com/en/user-guide/account-replication-intro)
### Step 7: Monitoring and cost management (Week 3) · Objective 2.3
 
- [ ] Compute, storage, serverless, and cloud services costs
- [ ] The 10% cloud services billing adjustment
- [ ] Resource monitors (warehouses) compared with budgets (broader, including serverless)
- [ ] `ACCOUNT_USAGE` compared with `INFORMATION_SCHEMA`: latency, retention, dropped objects
- [ ] Practise credit calculations
References:
- [Understanding overall cost](https://docs.snowflake.com/en/user-guide/cost-understanding-overall) · [Compute cost](https://docs.snowflake.com/en/user-guide/cost-understanding-compute) · [Storage cost](https://docs.snowflake.com/en/user-guide/cost-understanding-data-storage)
- [Resource monitors](https://docs.snowflake.com/en/user-guide/resource-monitors) · [Controlling cost](https://docs.snowflake.com/en/user-guide/cost-controlling)
- [Exploring compute cost](https://docs.snowflake.com/en/user-guide/cost-exploring-compute) · [Account Usage](https://docs.snowflake.com/en/sql-reference/account-usage)
### Step 8: Loading and unloading (Week 4) · Objective 3.1
 
- [ ] Stages: user, table, named internal, external; server-side encryption
- [ ] File formats; supported formats for loading compared with unloading
- [ ] `PUT`, `GET`, `LIST`, `REMOVE`; `COPY INTO <table>` and `COPY INTO <location>`
- [ ] `ON_ERROR`, `VALIDATION_MODE`, `VALIDATE`, `FORCE`, `PURGE`, load metadata
- [ ] Directory tables; file sizing best practice
References:
- [Overview of data loading](https://docs.snowflake.com/en/user-guide/data-load-overview) · [Loading considerations](https://docs.snowflake.com/en/user-guide/data-load-considerations-load)
- [COPY INTO table](https://docs.snowflake.com/en/sql-reference/sql/copy-into-table) · [COPY INTO location](https://docs.snowflake.com/en/sql-reference/sql/copy-into-location)
- [Transforming data during a load](https://docs.snowflake.com/en/user-guide/data-load-transform)
- [Directory tables](https://docs.snowflake.com/en/user-guide/data-load-dirtables) † · [Data unloading](https://docs.snowflake.com/en/user-guide/data-unload-overview) †
**Lab:** upload a CSV with deliberate errors, run `VALIDATION_MODE`, load it with different `ON_ERROR` settings, then unload to Parquet.
 
### Step 9: Automated ingestion and connectivity (Week 4) · Objectives 3.2, 3.3
 
- [ ] Snowpipe (auto-ingest and REST API) compared with bulk `COPY` and Snowpipe Streaming
- [ ] Streams: types, metadata columns, offsets, staleness
- [ ] Tasks: schedules, task graphs, serverless or warehouse compute
- [ ] Dynamic tables and target lag
- [ ] Drivers, connectors, storage integration, API integration, Git integration
- [ ] Openflow was listed as not tested until globally generally available, so check the current guide
References:
- [Snowpipe](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-intro) · [Auto-ingest](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-auto) · [REST API](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-rest-overview) · [Costs](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-billing)
- [Snowpipe Streaming](https://docs.snowflake.com/en/user-guide/data-load-snowpipe-streaming-overview)
- [Streams](https://docs.snowflake.com/en/user-guide/streams-intro) · [Tasks](https://docs.snowflake.com/en/user-guide/tasks-intro) †
- [Dynamic table target lag](https://docs.snowflake.com/en/user-guide/dynamic-tables/target-lag) · [Dynamic tables, streams and tasks, or materialized views](https://docs.snowflake.com/en/user-guide/dynamic-tables/decision-guide)
- [Drivers](https://docs.snowflake.com/en/developer-guide/drivers) † · [Storage integration for S3](https://docs.snowflake.com/en/user-guide/data-load-s3-config-storage-integration) † · [Git integration](https://docs.snowflake.com/en/developer-guide/git/git-overview) †
### Step 10: Performance and caching (Week 5) · Objectives 4.1–4.3
 
- [ ] Query Profile and Query Insights: spilling, pruning, exploding joins, queuing
- [ ] Query history and query attribution views
- [ ] Query acceleration, search optimization, clustering keys, materialized views: when to use each
- [ ] Result cache, metadata cache, warehouse cache
- [ ] Workload management: group similar workloads
 
References:
- [Optimizing query performance](https://docs.snowflake.com/en/user-guide/performance-query-options) · [Optimizing storage for performance](https://docs.snowflake.com/en/user-guide/performance-query-storage)
- [Query Profile](https://docs.snowflake.com/en/user-guide/ui-query-profile) †
- [Query Acceleration Service](https://docs.snowflake.com/en/user-guide/query-acceleration-service) · [Search optimization](https://docs.snowflake.com/en/user-guide/search-optimization-service) · [Clustering keys](https://docs.snowflake.com/en/user-guide/tables-clustering-keys) †
- [Persisted query results](https://docs.snowflake.com/en/user-guide/querying-persisted-results) · [RESULT_SCAN](https://docs.snowflake.com/en/sql-reference/functions/result_scan)
**Lab:** run a query on `SNOWFLAKE_SAMPLE_DATA` twice, compare the profiles, then set `USE_CACHED_RESULT = FALSE` and run it again.
 
### Step 11: Querying and transformation (Week 5) · Objective 4.4
 
- [ ] Structured, semi-structured (`VARIANT`, `FLATTEN`), and unstructured data
- [ ] Aggregate and window functions, `QUALIFY`
??? from here until ???END lines may have been inserted/deleted
- [ ] SQL habits that improve performance
- [ ] UDFs and stored procedures
References:
- [Querying semi-structured data](https://docs.snowflake.com/en/user-guide/querying-semistructured) † · [FLATTEN](https://docs.snowflake.com/en/sql-reference/functions/flatten) †
- [Window functions](https://docs.snowflake.com/en/user-guide/functions-window-using) †
- [Unstructured data](https://docs.snowflake.com/en/user-guide/unstructured-intro)
### Step 12: Data protection and collaboration (Week 6) · Objectives 5.1–5.3
 
- [ ] Time Travel, Fail-safe, `UNDROP`, zero-copy cloning
- [ ] Replication and failover
- [ ] Secure Data Sharing: providers, consumers, reader accounts, direct shares, resharing
- [ ] Data clean rooms
- [ ] Marketplace, public and private listings, Native Apps
References:
- [Time Travel](https://docs.snowflake.com/en/user-guide/data-time-travel) † · [Fail-safe](https://docs.snowflake.com/en/user-guide/data-failsafe) † · [Cloning](https://docs.snowflake.com/en/user-guide/object-clone) †
- [Storage costs for Time Travel and Fail-safe](https://docs.snowflake.com/en/user-guide/data-cdp-storage-costs)
- [Secure Data Sharing](https://docs.snowflake.com/en/user-guide/data-sharing-intro) · [Create shares](https://docs.snowflake.com/en/user-guide/data-sharing-provider) · [Consume shared data](https://docs.snowflake.com/en/user-guide/ 
???END
