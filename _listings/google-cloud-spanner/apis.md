---
name: Google Cloud Spanner
x-slug: google-cloud-spanner
description: 'Cloud Spanner is the first and only relational database service that
  is both strongly consistent and horizontally scalable. With Cloud Spanner you enjoy
  all the traditional benefits of a relational database: ACID transactions, relational
  schemas (and schema changes without downtime), SQL queries, high performance, and
  high availability. But unlike any other relational database service, Cloud Spanner
  scales horizontally, to hundreds or thousands of servers, so it can handle the highest
  of transactional workloads. With automatic scaling, synchronous data replication,
  and node redundancy, Cloud Spanner delivers up to 99.999% (five 9s) of availability
  for your mission critical applications. In fact, Google&rsquo;s internal Spanner
  service has been handling millions of queries per second from many Google services
  for years.'
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Google Cloud Spanner
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/apis.md
specificationVersion: "0.14"
apis:
- name: Cloud Spanner - Delete Database
  x-api-slug: v1database-delete
  description: Drops (aka deletes) a Cloud Spanner database.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1database-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1database-delete-openapi.md
- name: Cloud Spanner - Get Database Schema
  x-api-slug: v1databaseddl-get
  description: |-
    Returns the schema of a Cloud Spanner database as a list of formatted
    DDL statements. This method does not show pending schema updates, those may
    be queried using the Operations API.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1databaseddl-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1databaseddl-get-openapi.md
- name: Cloud Spanner - Update Database Schema
  x-api-slug: v1databaseddl-patch
  description: |-
    Updates the schema of a Cloud Spanner database by
    creating/altering/dropping tables, columns, indexes, etc. The returned
    long-running operation will have a name of
    the format `<database_name>/operations/<operation_id>` and can be used to
    track execution of the schema change(s). The
    metadata field type is
    UpdateDatabaseDdlMetadata.  The operation has no response.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1databaseddl-patch-openapi.md
- name: Cloud Spanner - Create Session
  x-api-slug: v1databasesessions-post
  description: |-
    Creates a new session. A session can be used to perform
    transactions that read and/or modify data in a Cloud Spanner database.
    Sessions are meant to be reused for many consecutive
    transactions.

    Sessions can only execute one transaction at a time. To execute
    multiple concurrent read-write/write-only transactions, create
    multiple sessions. Note that standalone reads and queries use a
    transaction internally, and count toward the one transaction
    limit.

    Cloud Spanner limits the number of sessions that can exist at any given
    time; thus, it is a good idea to delete idle and/or unneeded sessions.
    Aside from explicit deletes, Cloud Spanner can delete sessions for
    which no operations are sent for more than an hour, or due to
    internal errors. If a session is deleted, requests to it
    return `NOT_FOUND`.

    Idle sessions can be kept alive by sending a trivial SQL query
    periodically, e.g., `"SELECT 1"`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1databasesessions-post-openapi.md
- name: Cloud Spanner - End Session
  x-api-slug: v1name-delete
  description: Ends a session, releasing server resources associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1name-delete-openapi.md
- name: Cloud Spanner - Get Session
  x-api-slug: v1name-get
  description: |-
    Gets a session. Returns `NOT_FOUND` if the session does not exist.
    This is mainly useful for determining whether a session is still
    alive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1name-get-openapi.md
- name: Cloud Spanner - Update Instance
  x-api-slug: v1name-patch
  description: |-
    Updates an instance, and begins allocating or releasing resources
    as requested. The returned long-running
    operation can be used to track the
    progress of updating the instance. If the named instance does not
    exist, returns `NOT_FOUND`.

    Immediately upon completion of this request:

      * For resource types for which a decrease in the instance's allocation
        has been requested, billing is based on the newly-requested level.

    Until completion of the returned operation:

      * Cancelling the operation sets its metadata's
        cancel_time, and begins
        restoring resources to their pre-request values. The operation
        is guaranteed to succeed at undoing all resource changes,
        after which point it terminates with a `CANCELLED` status.
      * All other attempts to modify the instance are rejected.
      * Reading the instance via the API continues to give the pre-request
        resource levels.

    Upon completion of the returned operation:

      * Billing begins for all successfully-allocated resources (some types
        may have lower than the requested levels).
      * All newly-reserved resources are available for serving the instance's
        tables.
      * The instance's new resource levels are readable via the API.

    The returned long-running operation will
    have a name of the format `<instance_name>/operations/<operation_id>` and
    can be used to track the instance modification.  The
    metadata field type is
    UpdateInstanceMetadata.
    The response field type is
    Instance, if successful.

    Authorization requires `spanner.instances.update` permission on
    resource name.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1name-patch-openapi.md
- name: Cloud Spanner - Cancel Instance
  x-api-slug: v1namecancel-post
  description: |-
    Starts asynchronous cancellation on a long-running operation.  The server
    makes a best effort to cancel the operation, but success is not
    guaranteed.  If the server doesn't support this method, it returns
    `google.rpc.Code.UNIMPLEMENTED`.  Clients can use
    Operations.GetOperation or
    other methods to check whether the cancellation succeeded or whether the
    operation completed despite cancellation. On successful cancellation,
    the operation is not deleted; instead, it becomes an operation with
    an Operation.error value with a google.rpc.Status.code of 1,
    corresponding to `Code.CANCELLED`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1namecancel-post-openapi.md
- name: Cloud Spanner - Get Databases
  x-api-slug: v1parentdatabases-get
  description: Lists Cloud Spanner databases.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentdatabases-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentdatabases-get-openapi.md
- name: Cloud Spanner - Create Database
  x-api-slug: v1parentdatabases-post
  description: |-
    Creates a new Cloud Spanner database and starts to prepare it for serving.
    The returned long-running operation will
    have a name of the format `<database_name>/operations/<operation_id>` and
    can be used to track preparation of the database. The
    metadata field type is
    CreateDatabaseMetadata. The
    response field type is
    Database, if successful.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentdatabases-post-openapi.md
- name: Cloud Spanner - Get Instance Configurations
  x-api-slug: v1parentinstanceconfigs-get
  description: Lists the supported instance configurations for a given project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentinstanceconfigs-get-openapi.md
- name: Cloud Spanner - Get Instances
  x-api-slug: v1parentinstances-get
  description: Lists all instances in the given project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentinstances-get-openapi.md
- name: Cloud Spanner - Create instance
  x-api-slug: v1parentinstances-post
  description: |-
    Creates an instance and begins preparing it to begin serving. The
    returned long-running operation
    can be used to track the progress of preparing the new
    instance. The instance name is assigned by the caller. If the
    named instance already exists, `CreateInstance` returns
    `ALREADY_EXISTS`.

    Immediately upon completion of this request:

      * The instance is readable via the API, with all requested attributes
        but no allocated resources. Its state is `CREATING`.

    Until completion of the returned operation:

      * Cancelling the operation renders the instance immediately unreadable
        via the API.
      * The instance can be deleted.
      * All other attempts to modify the instance are rejected.

    Upon completion of the returned operation:

      * Billing for all successfully-allocated resources begins (some types
        may have lower than the requested levels).
      * Databases can be created in the instance.
      * The instance's allocated resource levels are readable via the API.
      * The instance's state becomes `READY`.

    The returned long-running operation will
    have a name of the format `<instance_name>/operations/<operation_id>` and
    can be used to track creation of the instance.  The
    metadata field type is
    CreateInstanceMetadata.
    The response field type is
    Instance, if successful.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1parentinstances-post-openapi.md
- name: Cloud Spanner - Get IAM Policy
  x-api-slug: v1resourcegetiampolicy-post
  description: |-
    Gets the access control policy for a database resource. Returns an empty
    policy if a database exists but does not have a policy set.

    Authorization requires `spanner.databases.getIamPolicy` permission on
    resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1resourcegetiampolicy-post-openapi.md
- name: Cloud Spanner - Set IAM Policy
  x-api-slug: v1resourcesetiampolicy-post
  description: |-
    Sets the access control policy on a database resource. Replaces any
    existing policy.

    Authorization requires `spanner.databases.setIamPolicy` permission on
    resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1resourcesetiampolicy-post-openapi.md
- name: Cloud Spanner - Test IAM Permissions
  x-api-slug: v1resourcetestiampermissions-post
  description: |-
    Returns permissions that the caller has on the specified database resource.

    Attempting this RPC on a non-existent Cloud Spanner database will result in
    a NOT_FOUND error if the user has `spanner.databases.list` permission on
    the containing Cloud Spanner instance. Otherwise returns an empty set of
    permissions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1resourcetestiampermissions-post-openapi.md
- name: Cloud Spanner - Begin Transaction
  x-api-slug: v1sessionbegintransaction-post
  description: |-
    Begins a new transaction. This step can often be skipped:
    Read, ExecuteSql and
    Commit can begin a new transaction as a
    side-effect.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionbegintransaction-post-openapi.md
- name: Cloud Spanner - Commit Transaction
  x-api-slug: v1sessioncommit-post
  description: |-
    Commits a transaction. The request includes the mutations to be
    applied to rows in the database.

    `Commit` might return an `ABORTED` error. This can occur at any time;
    commonly, the cause is conflicts with concurrent
    transactions. However, it can also happen for a variety of other
    reasons. If `Commit` returns `ABORTED`, the caller should re-attempt
    the transaction from the beginning, re-using the same session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessioncommit-post-openapi.md
- name: Cloud Spanner - Execute SQL
  x-api-slug: v1sessionexecutesql-post
  description: |-
    Executes an SQL query, returning all rows in a single reply. This
    method cannot be used to return a result set larger than 10 MiB;
    if the query yields more data than that, the query fails with
    a `FAILED_PRECONDITION` error.

    Queries inside read-write transactions might return `ABORTED`. If
    this occurs, the application should restart the transaction from
    the beginning. See Transaction for more details.

    Larger result sets can be fetched in streaming fashion by calling
    ExecuteStreamingSql instead.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionexecutesql-post-openapi.md
- name: Cloud Spanner - Execute Streaming SQL
  x-api-slug: v1sessionexecutestreamingsql-post
  description: |-
    Like ExecuteSql, except returns the result
    set as a stream. Unlike ExecuteSql, there
    is no limit on the size of the returned result set. However, no
    individual row in the result set can exceed 100 MiB, and no
    column value can exceed 10 MiB.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionexecutestreamingsql-post-openapi.md
- name: Cloud Spanner - Read Rows
  x-api-slug: v1sessionread-post
  description: |-
    Reads rows from the database using key lookups and scans, as a
    simple key/value style alternative to
    ExecuteSql.  This method cannot be used to
    return a result set larger than 10 MiB; if the read matches more
    data than that, the read fails with a `FAILED_PRECONDITION`
    error.

    Reads inside read-write transactions might return `ABORTED`. If
    this occurs, the application should restart the transaction from
    the beginning. See Transaction for more details.

    Larger result sets can be yielded in streaming fashion by calling
    StreamingRead instead.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionread-post-openapi.md
- name: Cloud Spanner - Rollback Transaction
  x-api-slug: v1sessionrollback-post
  description: |-
    Rolls back a transaction, releasing any locks it holds. It is a good
    idea to call this for any transaction that includes one or more
    Read or ExecuteSql requests and
    ultimately decides not to commit.

    `Rollback` returns `OK` if it successfully aborts the transaction, the
    transaction was already aborted, or the transaction is not
    found. `Rollback` never returns `ABORTED`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionrollback-post-openapi.md
- name: Cloud Spanner - Streaming Read
  x-api-slug: v1sessionstreamingread-post
  description: |-
    Like Read, except returns the result set as a
    stream. Unlike Read, there is no limit on the
    size of the returned result set. However, no individual row in
    the result set can exceed 100 MiB, and no column value can exceed
    10 MiB.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-spanner/master/_listings/google-cloud-spanner/v1sessionstreamingread-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.cloud.source.repositories.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.cloud.spanner.stack.network
- type: x-change-log
  url: https://cloud.google.com/spanner/docs/release-notes
- type: x-code
  url: https://cloud.google.com/spanner/docs/reference/libraries
- type: x-command-line-interfaces
  url: https://cloud.google.com/spanner/docs/gcloud-spanner
- type: x-concepts
  url: https://cloud.google.com/spanner/docs/concepts
- type: x-documentation
  url: https://cloud.google.com/spanner/docs/
- type: x-getting-started
  url: https://cloud.google.com/spanner/docs/quickstart-console
- type: x-guide
  url: https://cloud.google.com/spanner/docs/how-to
- type: x-pricing
  url: https://cloud.google.com/spanner/pricing
- type: x-rate-limits
  url: https://cloud.google.com/spanner/docs/limits
- type: x-schema
  url: https://cloud.google.com/spanner/docs/information-schema
- type: x-service-level-agreements
  url: https://cloud.google.com/spanner/sla
- type: x-support
  url: https://cloud.google.com/spanner/docs/support
- type: x-website
  url: https://cloud.google.com/spanner/
- type: x-white-papers
  url: https://cloud.google.com/spanner/docs/whitepapers
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---