## Part 4: Practice quiz (150 questions)
 
Choose **one** answer per question. Record your answers separately, then check the appendix. Questions about warehouse credits assume Gen1 warehouses.
 
### Domain 1: Snowflake AI Data Cloud Features and Architecture
 
**Q1.** Which layer of the Snowflake architecture handles authentication, metadata management, and query optimization?
 
- A. Compute
- B. Cloud services
- C. Database storage
- D. Client connectivity
**Q2.** Which statement best describes Snowflake's architecture?
 
- A. Shared-nothing, with each node permanently owning a slice of the data
- B. A single-server database with read replicas
- C. Shared-disk, with a single compute cluster serving all users
- D. Multi-cluster, shared data, with storage and compute scaling independently
**Q3.** Where is the processing for a user's SELECT statement that scans table data performed?
 
- A. In the database storage layer
- B. In a virtual warehouse
- C. On the client machine
- D. In the stage that holds the source files
**Q4.** What is the minimum Snowflake edition that supports multi-cluster warehouses?
 
- A. Business Critical
- B. Virtual Private Snowflake
- C. Enterprise
- D. Standard
**Q5.** A company must store protected health information (PHI) subject to HIPAA. What is the minimum edition?
 
- A. Any edition with a network policy
- B. Standard
- C. Business Critical
- D. Enterprise
**Q6.** Which of these features is available in Standard Edition?
 
- A. Dynamic tables
- B. Materialized views
- C. Query acceleration service
- D. Search optimization service
**Q7.** Which edition provides a Snowflake environment completely separated from other Snowflake accounts?
 
- A. Virtual Private Snowflake (VPS)
- B. Business Critical
- C. Standard
- D. Enterprise
**Q8.** What is Snowsight?
 
- A. A command-line client that must be installed on each user's local machine
- B. A driver that connects Java applications to a Snowflake account
- C. A serverless service that continuously loads files from external stages
- D. Snowflake's web interface for querying, monitoring, and administration
**Q9.** Which tool lets a developer manage Snowflake workloads from a terminal using the `snow` command?
 
- A. Snowflake CLI
- B. Snowsight
- C. Query Profile
- D. Snowpipe
**Q10.** A developer wants to write and run Snowflake SQL inside a local code editor. Which option fits best?
 
- A. A directory table enabled on an internal stage
- B. The Snowflake extension for Visual Studio Code
- C. A reader account created by the data provider
- D. A resource monitor assigned to the developer's warehouse
**Q11.** Which is the correct object hierarchy, from highest to lowest?
 
- A. Account, schema, database, organization, table
- B. Organization, account, database, schema, table
- C. Organization, database, account, schema, table
- D. Account, organization, schema, database, table
**Q12.** Which of the following is an account-level object rather than a schema-level object?
 
- A. File format
- B. Virtual warehouse
- C. Sequence
- D. Stage
**Q13.** A parameter is set at the account level, then set to a different value for a user, then changed again in that user's current session. Which value applies in the session?
 
- A. The account value
- B. The lowest numeric value of the three
- C. The session value
- D. The user value
**Q14.** DATA_RETENTION_TIME_IN_DAYS is 10 on a database, and 3 on one table inside it. What is the table's retention period?
 
- A. 3 days
- B. 10 days
- C. 13 days
- D. 1 day
**Q15.** Which statement defines a session variable that can later be referenced as $region?
 
- A. ALTER SESSION SET region = 'APAC';
- B. SET region = 'APAC';
- C. DECLARE SESSION region = 'APAC';
- D. CREATE VARIABLE region = 'APAC';
**Q16.** Which expression returns the role currently in use as the primary role?
 
- A. ACTIVE_USER()
- B. CURRENT_ROLE()
- C. SESSION_ROLE_ID()
- D. SHOW ROLE()
**Q17.** Which statement about micro-partitions is correct?
 
- A. Users must define their boundaries by declaring a partition key
- B. Snowflake edits them in place whenever the rows inside them change
- C. Snowflake creates them automatically and stores data in columnar form
- D. Each one holds exactly 1 GB of uncompressed data in row-based form
**Q18.** What is the approximate uncompressed data size of a micro-partition?
 
- A. 1 MB to 5 MB
- B. 1 GB to 5 GB
- C. Fixed at 16 MB
- D. 50 MB to 500 MB
**Q19.** What happens when rows in a table are updated?
 
- A. New micro-partitions are written to replace the affected ones
- B. Changes are held only in the warehouse cache
- C. The existing micro-partition files are edited in place
- D. The whole table is always rewritten
**Q20.** How does Snowflake use micro-partition metadata, such as the range of values in each column?
 
- A. To encrypt each column with a key chosen by the user
- B. To enforce primary key uniqueness during inserts
- C. To skip partitions that cannot match a query filter
- D. To choose the warehouse size needed for each query
**Q21.** When is defining a clustering key most likely to be worthwhile?
 
- A. On a table that is truncated and fully reloaded every few minutes
- B. On every small lookup table that is joined to a large fact table
- C. On a table whose queries always read all rows without any filter
- D. On a very large table that is often filtered on the same columns and prunes poorly
**Q22.** For a well-clustered table on a given set of columns, what would you expect of the average clustering depth?
 
- A. It is small
- B. It is large
- C. It equals the warehouse size
- D. It equals the number of rows
**Q23.** Which table type persists only for the session that created it?
 
- A. Transient
- B. Permanent
- C. External
- D. Temporary
**Q24.** A staging table must persist across sessions but does not need Fail-safe protection. Which type fits best?
 
- A. External
- B. Permanent
- C. Transient
- D. Temporary
**Q25.** Which table type is created when CREATE TABLE is run in a permanent schema with no type keyword?
 
- A. Temporary
- B. Transient
- C. Dynamic
- D. Permanent
**Q26.** Which statement about standard external tables is correct?
 
- A. They keep dropped files recoverable through seven-day Fail-safe
- B. They let you query files in external storage and are read-only
- C. They support UPDATE and DELETE on the underlying files
- D. They copy files into micro-partitions before any query can run
**Q27.** What is a defining feature of Apache Iceberg tables in Snowflake?
 
- A. They store rows only for the duration of the session that created them
- B. They accept only JSON documents held in a single VARIANT column
- C. They use an open table format for data and metadata files in cloud storage
- D. They are materialized views that are refreshed on a user-defined schedule
**Q28.** Which object automatically materializes the result of a query and keeps it refreshed to meet a data freshness target?
 
- A. Sequence
- B. Dynamic table
- C. Temporary table
- D. Standard view
**Q29.** Which statement about a standard (non-materialized) view is correct?
 
- A. It stores a physical copy of the results, which is read when referenced
- B. It stores results that a serverless service refreshes when base tables change
- C. It stores the query definition, and the query runs when the view is referenced
- D. It can be created only in accounts on Enterprise Edition or higher
**Q30.** Which is a limitation of Snowflake materialized views?
 
- A. The defining table can never have a clustering key applied
- B. The defining query can reference only a single table
- C. They can be created only on top of temporary tables
- D. Users must schedule a task to refresh the stored results
**Q31.** Why would a data provider choose a secure view instead of a standard view?
 
- A. To allow consumer accounts to update rows in the provider's base tables
- B. To make queries run faster by exposing the definition to the optimizer
- C. To hide the view definition and prevent data exposure through certain optimizations
- D. To store the query results physically and refresh them automatically
**Q32.** How many credits per hour does a single-cluster Large Gen1 warehouse consume?
 
- A. 16
- B. 10
- C. 8
- D. 4
**Q33.** A query is complex and slow on a Small warehouse, with no queuing. Which change is the most appropriate first step?
 
- A. Increase the warehouse size
- B. Lower the auto-suspend time
- C. Add more clusters of the same size
- D. Create a reader account
**Q34.** Many users run short dashboard queries at 9 a.m. and the queries queue. Which solution fits best?
 
- A. Increase Time Travel retention
- B. Convert the tables to transient
- C. Disable auto-resume
- D. Use a multi-cluster warehouse in auto-scale mode
**Q35.** Which multi-cluster configuration runs the warehouse in Maximized mode?
 
- A. SCALING_POLICY is set to ECONOMY while MIN_CLUSTER_COUNT is set to 1
- B. MIN_CLUSTER_COUNT is set to 1 and MAX_CLUSTER_COUNT is set higher than 1
- C. MIN_CLUSTER_COUNT and MAX_CLUSTER_COUNT are both left at a value of 1
- D. MIN_CLUSTER_COUNT equals MAX_CLUSTER_COUNT, and both are greater than 1
**Q36.** Which scaling policy favours keeping running clusters fully loaded to conserve credits?
 
- A. Serverless
- B. Maximized
- C. Economy
- D. Standard
**Q37.** What does AUTO_SUSPEND = 300 mean for a warehouse?
 
- A. It suspends after 300 minutes of inactivity
- B. It suspends after 300 seconds of inactivity
- C. It cancels queries that run longer than 300 seconds
- D. It suspends after consuming 300 credits
**Q38.** A warehouse is resized while a query is running. What happens to that query?
 
- A. It is cancelled and then restarted automatically on the warehouse at its new size
- B. It pauses, moves to the new resources, and continues from where it stopped
- C. It finishes on the original resources, and the new size applies to queued and new queries
- D. It fails with an error, and the user must submit the statement again
**Q39.** Which warehouse type is designed for memory-intensive work such as single-node machine learning training?
 
- A. A multi-cluster Economy warehouse
- B. Snowpark-optimized
- C. A reader warehouse
- D. A standard X-Small warehouse
**Q40.** What best describes a Gen2 standard warehouse?
 
- A. A secondary warehouse that runs only after a failover to another region
- B. A newer generation of standard warehouse with upgraded hardware and performance improvements
- C. A warehouse that keeps a second synchronized copy of all table data for recovery
- D. A serverless warehouse that runs queries without consuming any compute credits
**Q41.** A team wants ETL jobs not to slow down BI dashboards. What is the best practice?
 
- A. Copy the data into a second account for dashboards
- B. Turn off the result cache for the ETL users
- C. Run both workloads on one shared X-Small warehouse
- D. Run each workload on a separate warehouse
**Q42.** Which feature lets users combine SQL, Python, and Markdown cells interactively within Snowflake?
 
- A. Directory tables
- B. Snowpipe
- C. Resource monitors
- D. Snowflake Notebooks
**Q43.** A team wants to build an interactive data app in Python that runs inside Snowflake. Which feature should they use?
 
- A. Fail-safe
- B. Cortex Search
- C. Search optimization service
- D. Streamlit in Snowflake
**Q44.** What does Snowpark provide?
 
- A. A firewall service that restricts which networks can reach a Snowflake account
- B. A marketplace where accounts can buy and sell prepared data sets and applications
- C. Libraries to process data with languages such as Python, Java, and Scala inside Snowflake
- D. A backup service that restores dropped tables after their retention period ends
**Q45.** Business users want to ask questions in natural language and receive answers generated as SQL over structured data. Which feature is designed for this?
 
- A. Cortex Search
- B. Query Profile
- C. Cortex Analyst
- D. Snowpipe Streaming
**Q46.** Which feature is designed for semantic and hybrid search over text data, for example to support a retrieval-augmented chatbot?
 
- A. Cortex Search
- B. Metadata cache
- C. Search optimization service
- D. Cortex Analyst
**Q47.** Which Snowflake capability covers building, registering, and managing machine learning models close to the governed data?
 
- A. Secure Data Sharing
- B. Snowpipe
- C. Snowflake ML
- D. Network policies
### Domain 2: Account Management and Data Governance
 
**Q48.** In role-based access control, how do users normally receive privileges on objects?
 
- A. All users receive every privilege, and administrators then revoke what is not needed
- B. Privileges are granted to roles, and roles are granted to users
- C. Privileges are defined in network policies that are then attached to each user
- D. Privileges are granted to warehouses, and users inherit them when running queries
**Q49.** Which concept means that each object has an owner who can grant access to it?
 
- A. Row-level security
- B. Discretionary access control (DAC)
- C. Zero-copy cloning
- D. Federated authentication
**Q50.** Which system role is recommended for creating and managing users and roles?
 
- A. PUBLIC
- B. ORGADMIN
- C. SYSADMIN
- D. USERADMIN
**Q51.** Which system role holds the global MANAGE GRANTS privilege by default and sits below ACCOUNTADMIN?
 
- A. USERADMIN
- B. SYSADMIN
- C. SECURITYADMIN
- D. PUBLIC
**Q52.** Which system role is intended for creating warehouses, databases, and other objects?
 
- A. USERADMIN
- B. SYSADMIN
- C. PUBLIC
- D. SECURITYADMIN
**Q53.** Which role is automatically granted to every user and role?
 
- A. SYSADMIN
- B. ACCOUNTADMIN
- C. PUBLIC
- D. USERADMIN
**Q54.** According to best practice, where should custom role hierarchies usually roll up?
 
- A. To PUBLIC
- B. To no other role
- C. To USERADMIN
- D. To SYSADMIN
**Q55.** Which statement about ACCOUNTADMIN is correct?
 
- A. It is the most powerful account role and should be granted to a limited number of users
- B. It should be set as the default role for every user who needs to query data
- C. It should own all routine database objects created by loading and ETL jobs
- D. It bypasses all privilege checks, including on objects it has no grants for
**Q56.** What distinguishes a database role from an account role?
 
- A. It is scoped to the whole organization and can create new accounts
- B. It owns every warehouse used to query the objects in its database
- C. It is scoped to one database and cannot be activated directly in a session
- D. It can be granted only directly to users, never to any other role
**Q57.** What do secondary roles allow?
 
- A. A session to create new objects that are owned jointly by all of the granted roles
- B. A session to use the combined privileges of additional granted roles for authorized actions
- C. A role from one account to be granted to users in any other Snowflake account
- D. A user to skip multi-factor authentication when switching between roles in one session
**Q58.** Which feature restricts access to Snowflake based on the originating IP address or network identifier?
 
- A. Resource monitor
- B. Row access policy
- C. Network policy
- D. Masking policy
**Q59.** A request comes from an IP address on a network policy's blocked list. What happens with the authentication policy?
 
- A. It is evaluated first and can override the block set by the network policy
- B. It is applied instead, and converts the login attempt to an OAuth flow
- C. It is evaluated afterwards and can allow the request if MFA succeeds
- D. It is not evaluated, because the network policy stops the request first
**Q60.** Which authentication method is most suitable for a non-interactive service connecting with a driver?
 
- A. Password with an interactive MFA prompt
- B. Sharing an administrator's password
- C. Browser-based SSO
- D. Key-pair authentication
**Q61.** A company wants employees to sign in to Snowflake through its corporate identity provider. Which capability is this?
 
- A. Federated authentication (single sign-on)
- B. Secondary roles
- C. Tri-Secret Secure
- D. Key rotation
**Q62.** What is Snowflake's direction for single-factor password sign-ins?
 
- A. Passwords alone remain sufficient for both human users and service users
- B. Human password users must use MFA, and service users cannot rely on passwords
- C. Service users keep passwords but must approve an SMS prompt at each login
- D. MFA is required only for users who hold ACCOUNTADMIN in Standard Edition
**Q63.** Which is the preferred account identifier format?
 
- A. region_only
- B. username@database
- C. warehouse.schema
- D. orgname-account_name
**Q64.** Where does Snowflake collect log messages and trace events emitted by handler code such as procedures and UDFs?
 
- A. In a transient stage
- B. In a directory table
- C. In the result cache
- D. In an event table
**Q65.** Which feature shows a masked or clear column value at query time depending on the querying context, without changing stored data?
 
- A. Dynamic data masking policy
- B. Clustering key
- C. Row access policy
- D. Network policy
**Q66.** Sales managers must see only the rows for their own region in one shared table. Which feature should be used?
 
- A. Row access policy
- B. Masking policy
- C. Resource monitor
- D. Search optimization
**Q67.** What is the main purpose of object tags?
 
- A. To classify and track objects and columns with key-value metadata
- B. To raise query concurrency on warehouses that carry a tag
- C. To compress the micro-partitions that belong to tagged tables
- D. To schedule SQL statements that run against tagged objects
**Q68.** A column has a directly assigned masking policy and is also covered by a tag-based masking policy. Which takes precedence?
 
- A. The tag-based policy
- B. The directly assigned masking policy
- C. Both run in sequence on every query
- D. Neither is applied
**Q69.** Which policy type requires queries on protected data to return results grouped into at least a minimum number of records?
 
- A. Aggregation policy
- B. Network policy
- C. Session policy
- D. Password policy
**Q70.** Which feature evaluates an account against security recommendations and reports findings through scanners?
 
- A. Query Profile
- B. Snowflake Marketplace
- C. Data lineage
- D. Trust Center
**Q71.** What does Tri-Secret Secure combine?
 
- A. Multi-factor authentication with a network policy and an authentication policy
- B. Three separate passwords that must all be entered by the account administrator
- C. A customer-managed key with a Snowflake-maintained key to protect data
- D. Three independent copies of each table stored in three different cloud regions
**Q72.** Which Snowflake object evaluates a condition on a schedule and performs an action when the condition is met?
 
- A. Sequence
- B. File format
- C. Stream
- D. Alert
**Q73.** A data steward needs to see which downstream objects are affected by a change to a source table. Which feature helps most?
 
- A. Data lineage
- B. Warehouse cache
- C. Fail-safe
- D. Resource monitor
**Q74.** Which actions can a resource monitor take when a threshold is reached?
 
- A. Mask, filter, or tag
- B. Resize, clone, or drop
- C. Notify, suspend, or suspend immediately
- D. Recluster, vacuum, or index
**Q75.** A Medium multi-cluster Gen1 warehouse runs 3 clusters continuously for 2 hours. How many credits are consumed?
 
- A. 24
- B. 12
- C. 8
- D. 48
**Q76.** On one day, warehouses use 100 credits and cloud services use 13 credits. How many cloud services credits are billed?
 
- A. 13
- B. 3
- C. 10
- D. 0
**Q77.** An analyst needs 12 months of query history, including activity on dropped objects. Where should they look?
 
- A. The warehouse cache
- B. SNOWFLAKE.ACCOUNT_USAGE views
- C. A directory table
- D. The database INFORMATION_SCHEMA
### Domain 3: Data Loading, Unloading, and Connectivity
 
**Q78.** Which notation refers to the current user's own stage?
 
- A. @#user
- B. @%orders
- C. @orders_stage
- D. @~
**Q79.** Which feature lets Snowflake fetch files from a remote source control repository so they can be referenced and executed?
 
- A. Directory table
- B. Storage integration
- C. Git integration
- D. Snowpipe auto-ingest
**Q80.** Which command uploads a file from a local machine to an internal stage?
 
- A. GET
- B. INSERT
- C. COPY INTO <table>
- D. PUT
**Q81.** Which command downloads files from an internal stage to a local machine?
 
- A. UNDROP
- B. LIST
- C. GET
- D. PUT
**Q82.** By default, what does PUT do with an uncompressed CSV file?
 
- A. Converts it to Parquet
- B. Compresses it with gzip during upload
- C. Deletes the local copy
- D. Loads it into a table
**Q83.** Which setting configures server-side encryption only on a Snowflake internal named stage?
 
- A. ENCRYPTION = (TYPE = 'SNOWFLAKE_SSE')
- B. FILE_FORMAT = (TYPE = 'SSE')
- C. ENCRYPTION = (TYPE = 'NONE')
- D. PURGE = TRUE
**Q84.** Which file format is supported for loading data but is NOT a supported unload format for COPY INTO <location>?
 
- A. JSON
- B. Parquet
- C. Avro
- D. CSV
**Q85.** What is the benefit of creating a named file format object?
 
- A. It removes the need for a stage
- B. It automatically loads new files
- C. Parsing options can be defined once and reused
- D. It encrypts the target table with a customer key
**Q86.** What is the general recommendation for data file size in bulk loading?
 
- A. At least 10 GB compressed
- B. Exactly 16 MB uncompressed
- C. Under 100 KB compressed
- D. About 100-250 MB compressed
**Q87.** A JSON file contains one large outer array of records. Which file format option loads each element as a separate row?
 
- A. SINGLE = TRUE
- B. STRIP_OUTER_ARRAY = TRUE
- C. SKIP_HEADER = 1
- D. FORCE = TRUE
**Q88.** What is the default ON_ERROR behaviour for bulk loading with COPY INTO <table>?
 
- A. CONTINUE
- B. ABORT_STATEMENT
- C. SKIP_FILE_10
- D. SKIP_FILE
**Q89.** What is the default ON_ERROR behaviour for Snowpipe?
 
- A. CONTINUE
- B. RETURN_ERRORS
- C. SKIP_FILE
- D. ABORT_STATEMENT

**Q90.** Which option checks staged files for errors without loading any rows?
 
- A. PURGE
- B. VALIDATION_MODE
- C. MATCH_BY_COLUMN_NAME
- D. FORCE
**Q91.** For how long is bulk load metadata kept on a target table?
 
- A. 64 days
- B. 365 days
- C. 7 days
- D. 14 days
**Q92.** A previously loaded, unchanged file must deliberately be loaded again with COPY INTO. Which option does this?
 
- A. ON_ERROR = CONTINUE
- B. FORCE = TRUE
- C. VALIDATION_MODE = RETURN_ERRORS
- D. PURGE = TRUE
**Q93.** What does PURGE = TRUE do in a COPY INTO <table> statement?
 
- A. Deletes load metadata so that the same files can be loaded again
- B. Removes files from the stage after they are loaded successfully
- C. Truncates the target table before the new files are loaded into it
- D. Removes the rows that contain errors from the staged source files
**Q94.** What is the default value of the SINGLE copy option when unloading data, and its effect?
 
- A. FALSE, so output may be split into multiple files
- B. FALSE, so only the first row of the result is exported
- C. TRUE, so each row is written to its own separate file
- D. TRUE, so the output is always written to exactly one file
**Q95.** What does a directory table provide?
 
- A. A list of all databases in an account
- B. Queryable file-level metadata about files on a stage
- C. A copy of every file's contents in VARIANT columns
- D. A history of role grants
**Q96.** Which statement about Snowpipe compute is correct?
 
- A. It runs on the client machine
- B. It requires a dedicated user-managed warehouse
- C. It uses only the warehouse of the user who staged the file
- D. It uses Snowflake-managed serverless compute
**Q97.** How can a Snowpipe pipe learn about new files?
 
- A. Cloud storage event notifications or calls to the Snowpipe REST API
- B. The query result cache
- C. Only a manual UNDROP command
- D. A resource monitor trigger
**Q98.** An application produces rows continuously and needs them queryable within seconds without staging files. What is the best choice?
 
- A. Bulk COPY INTO on an hourly schedule
- B. Snowpipe Streaming
- C. An external table with manual refresh
- D. Zero-copy cloning
**Q99.** What does a standard stream on a table record?
 
- A. Only changes made to the column names and data types of the source
- B. A full physical copy of the source table taken on an hourly schedule
- C. Row-level changes made to the source since the stream's offset
- D. The warehouse credits consumed by each change made to the source
**Q100.** What advances a stream's offset?
 
- A. Running a plain SELECT statement that reads every record in the stream
- B. Consuming the stream in a DML statement within a committed transaction
- C. Viewing the stream's details with the SHOW STREAMS command in a session
- D. Suspending and then resuming the warehouse that last queried the stream
**Q101.** Which WHEN condition lets a task run only if a stream contains change data?
 
- A. CURRENT_STREAM()
- B. SYSTEM$STREAM_HAS_DATA('my_stream')
- C. RESULT_SCAN('my_stream')
- D. SYSTEM$PIPE_STATUS('my_stream')
**Q102.** What is required after creating a new task before its schedule starts running it?
 
- A. Resume it, for example with ALTER TASK ... RESUME
- B. Add it to a share
- C. Run PUT on its definition
- D. Clone it
**Q103.** What does TARGET_LAG = '10 minutes' mean on a dynamic table?
 
- A. Any query on the table is cancelled if it runs longer than 10 minutes
- B. The table is guaranteed to refresh at exact 10-minute clock intervals
- C. The table keeps 10 minutes of historical data available for Time Travel
- D. The data should be no more than about 10 minutes behind its sources
**Q104.** Which object lets Snowflake access external cloud storage without placing secret keys in each stage definition?
 
- A. Resource monitor
- B. Directory table
- C. API integration
- D. Storage integration
### Domain 4: Performance Optimization, Querying, and Transformation
 
**Q105.** Which tool shows the operator tree and execution statistics for a completed query?
 
- A. Query Profile
- B. Resource monitor
- C. Directory table
- D. Trust Center
**Q106.** Query Profile shows a large amount of data spilled to remote storage. Which action is most likely to help?
 
- A. Use a larger warehouse or process the data in smaller batches
- B. Add a masking policy
- C. Reduce the warehouse size
- D. Increase the auto-suspend time only
**Q107.** Which is usually worse for performance?
 
- A. Reading from the warehouse cache
- B. Returning results from the result cache
- C. Spilling to remote storage
- D. Spilling to local disk
**Q108.** A Query Profile shows partitions scanned nearly equal to partitions total, although the filter returns very few rows. What does this indicate?
 
- A. A suspended warehouse
- B. A result cache hit
- C. Inefficient pruning
- D. Warehouse queuing
**Q109.** A join operator outputs vastly more rows than either input. What is the likely cause?
 
- A. A missing or non-selective join condition causing an exploding join
- B. The warehouse was suspended and resumed during the join
- C. Time Travel retention is set too high on both input tables
- D. Both input tables were created as transient tables
**Q110.** Query history shows long queued-overload time. Which change targets this problem?
 
- A. Add warehouse capacity for concurrency, such as more clusters
- B. Create a secure view
- C. Reduce the number of micro-partition columns
- D. Lengthen Fail-safe
**Q111.** Which view helps attribute warehouse compute cost to individual queries?
 
- A. ACCOUNT_USAGE.QUERY_ATTRIBUTION_HISTORY
- B. ACCOUNT_USAGE.GRANTS_TO_USERS
- C. INFORMATION_SCHEMA.FILE_FORMATS
- D. INFORMATION_SCHEMA.COLUMNS
**Q112.** Which source lists historical queries across the account with details such as execution time and bytes scanned?
 
- A. ACCOUNT_USAGE.TABLES
- B. ACCOUNT_USAGE.USERS
- C. ACCOUNT_USAGE.STAGES
- D. ACCOUNT_USAGE.QUERY_HISTORY
**Q113.** Which is a recommended workload management practice?
 
- A. Group similar workloads on appropriately sized warehouses
- B. Disable auto-suspend on all warehouses
- C. Give every query its own account
- D. Put all workloads on the largest warehouse permanently
**Q114.** Which parameter cancels a statement that runs longer than a specified number of seconds?
 
- A. STATEMENT_TIMEOUT_IN_SECONDS
- B. USE_CACHED_RESULT
- C. AUTO_SUSPEND
- D. DATA_RETENTION_TIME_IN_DAYS
**Q115.** Which workload is a good candidate for the query acceleration service?
 
- A. Occasional large scans with selective filters or aggregation
- B. Single-row lookups already served by metadata
- C. Queries waiting only on a table lock
- D. User authentication requests
**Q116.** Which service is designed to speed up highly selective point lookups on large tables?
 
- A. Query acceleration service
- B. Resource monitor
- C. Search optimization service
- D. Fail-safe
**Q117.** What data structure does the search optimization service maintain?
 
- A. A search access path
- B. A transient stage
- C. A user-managed B-tree index
- D. A stream offset
**Q118.** Dashboards repeatedly run the same expensive aggregation on one large table that changes infrequently. Which object can precompute it with automatic maintenance?
 
- A. Standard view
- B. Temporary stage
- C. Materialized view
- D. Sequence
**Q119.** What ongoing cost should be considered after defining a clustering key with automatic clustering?
 
- A. A per-user licence fee
- B. Reader account fees
- C. A charge for each SELECT permission grant
- D. Serverless compute for reclustering and possible extra storage
**Q120.** Which columns are generally the best candidates for a clustering key?
 
- A. A unique random identifier that is never filtered
- B. Every column in the table
- C. Columns never referenced by queries
- D. Columns frequently used in selective filters or joins
**Q121.** What is the base retention period of a persisted query result?
 
- A. 24 hours
- B. 7 days
- C. 1 hour
- D. 64 days
**Q122.** What is the maximum period to which repeated reuse can extend a persisted query result, measured from first execution?
 
- A. 64 days
- B. 31 days
- C. 90 days
- D. 7 days
**Q123.** Which condition generally allows a query result to be reused?
 
- A. The session has the USE_CACHED_RESULT parameter set to FALSE
- B. The underlying tables were modified after the query first ran
- C. The query calls a function that returns a new random value each run
- D. The query matches a previous one and the underlying data has not changed
**Q124.** Which cache resides on the local disk of a running virtual warehouse?
 
- A. Metadata cache
- B. Warehouse (data) cache
- C. Fail-safe cache
- D. Query result cache
**Q125.** What generally happens to the warehouse cache when a warehouse is suspended?
 
- A. It is saved as a materialized view that later queries read automatically
- B. It is moved into Fail-safe, where only Snowflake Support can restore it
- C. It is preserved for 31 days and reused by any other warehouse in the account
- D. It is dropped, so later queries may need to read from remote storage again
**Q126.** Which query can often be answered from metadata alone, without warehouse compute?
 
- A. SELECT COUNT(*) FROM sales;
- B. SELECT a.* FROM sales a JOIN stores b ON a.store_id = b.id;
- C. SELECT * FROM sales ORDER BY amount;
- D. SELECT customer, SUM(amount) FROM sales GROUP BY customer;
**Q127.** A VARIANT column V holds {"customer": {"name": "Ana"}}. Which expression returns the name as a string?
 
- A. v.customer:name
- B. v[customer][name]::STRING
- C. v->customer->name
- D. v:customer.name::STRING
**Q128.** Which function explodes a JSON array into multiple rows?
 
- A. PARSE_JSON
- B. OBJECT_CONSTRUCT
- C. LISTAGG
- D. FLATTEN
 
**Q129.** Which function converts a JSON-formatted string into a VARIANT value?
 
- A. TO_CHAR
- B. ARRAY_SIZE
- C. FLATTEN
- D. PARSE_JSON
**Q130.** Which clause filters rows based on the result of a window function?
 
- A. QUALIFY
- B. PIVOT
- C. HAVING
- D. WHERE
**Q131.** Two rows tie for first place. Which function assigns the next row a rank of 2, leaving no gap?
 
- A. RANK()
- B. DENSE_RANK()
- C. COUNT(*)
- D. ROW_NUMBER()
**Q132.** A column contains the values 10, NULL, and 20. What does COUNT(column) return?
 
- A. 2
- B. 3
- C. NULL
- D. 30
**Q133.** Which function gives a fast, approximate distinct count on a very large data set?
 
- A. MEDIAN
- B. COUNT(*)
- C. ROW_NUMBER
- D. APPROX_COUNT_DISTINCT
**Q134.** When duplicate rows do not need to be removed while combining two result sets, which operator avoids unnecessary work?
 
- A. INTERSECT
- B. MINUS
- C. UNION ALL
- D. UNION
**Q135.** Which function creates a time-limited web URL that can be used to download a staged file?
 
- A. SYSTEM$STREAM_HAS_DATA
- B. PARSE_JSON
- C. GET_PRESIGNED_URL
- D. RESULT_SCAN
### Domain 5: Data Collaboration
 
**Q136.** What is zero-copy cloning?
 
- A. Exporting an object to compressed files that can be reloaded later
- B. Creating a new object that initially references existing micro-partitions
- C. Copying every file immediately into a new, fully independent object
- D. Creating a replica in another region that uses no storage of its own
**Q137.** What is the minimum edition required for failover groups, used to fail over account workloads to another region or cloud?
 
- A. Any edition that has Time Travel
- B. Standard
- C. Business Critical
- D. Enterprise
**Q138.** What is the default Time Travel retention period?
 
- A. 0 days
- B. 7 days
- C. 90 days
- D. 1 day
**Q139.** What is the maximum Time Travel retention for a permanent table in Enterprise Edition?
 
- A. 90 days
- B. 365 days
- C. 1 day
- D. 7 days
**Q140.** What is the Fail-safe period for permanent tables?
 
- A. 7 days
- B. 1 day
- C. 90 days
- D. 14 days
**Q141.** Who can recover data that is in Fail-safe?
 
- A. The table owner using BEFORE
- B. Only Snowflake, upon request
- C. Any user with SELECT
- D. SYSADMIN using UNDROP
**Q142.** Which statement restores a dropped table that is still within its Time Travel retention period?
 
- A. RESTORE TABLE orders;
- B. UNDROP TABLE orders;
- C. RECOVER TABLE orders FROM FAILSAFE;
- D. ROLLBACK DROP orders;
**Q143.** Which clause queries a table as it existed immediately before a specific statement ran?
 
- A. HISTORY (QUERY => '<query_id>')
- B. AS OF FAILSAFE '<query_id>'
- C. AFTER (STATEMENT => '<query_id>')
- D. BEFORE (STATEMENT => '<query_id>')
**Q144.** In a standard (non-reader) data share, who pays for the compute used to query shared data?
 
- A. Snowflake, at no charge
- B. The provider
- C. Both are billed the full amount
- D. The consumer
**Q145.** How is data delivered through direct Secure Data Sharing within the same region?
 
- A. The consumer signs in to the provider account with a provider-managed role
- B. A full editable copy of the data is loaded into the consumer's account
- C. Consumers access the provider's data without it being copied, with read-only access
- D. Files are exported to a stage, and the consumer loads them on a schedule
**Q146.** A provider wants to share data with a partner that has no Snowflake account. What can the provider create?
 
- A. A directory table
- B. A reader account
- C. A transient account role
- D. A resource monitor only
**Q147.** Which statement about reader accounts is correct?
 
- A. They can consume shares from any provider
- B. They are mainly for uploading new data to the provider
- C. The provider is responsible for their credit charges
- D. The reader pays Snowflake directly under its own contract
**Q148.** What is a listing?
 
- A. The set of file names and sizes returned when a user runs the LIST command on a stage
- B. A backup copy of a database that Snowflake keeps available during the Fail-safe period
- C. A data product or Native App packaged with metadata and offered privately or on the Marketplace
- D. A record of failed queries and logins that is published to account administrators
**Q149.** What is the main purpose of a data clean room?
 
- A. To let parties analyze combined data under controls without exposing raw data to each other
- B. To give every party a full copy of the others' raw data inside one common account
- C. To remove duplicate and invalid rows from data sets automatically before they are shared
- D. To purge expired micro-partitions securely once their retention period has ended
**Q150.** Which statement about the Snowflake Native App Framework is correct?
 
- A. Providers can package application logic and data and distribute the app through listings
- B. It replaces the consumer's virtual warehouses with compute on the user's own device
- C. It requires consumers to send their raw data into the provider's account for processing
- D. It is a desktop client that providers install so that consumers can open Snowsight



