---
swagger: "2.0"
x-collection-name: Google Cloud Spanner
x-complete: 0
info:
  title: Google Cloud Spanner API Update Instance
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
  contact:
    name: Google
    url: https://google.com
  version: v1
host: spanner.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{database}:
    delete:
      summary: Delete Database
      description: Drops (aka deletes) a Cloud Spanner database.
      operationId: spanner.projects.instances.databases.dropDatabase
      x-api-path-slug: v1database-delete
      parameters:
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Database
  /v1/{database}/ddl:
    get:
      summary: Get Database Schema
      description: |-
        Returns the schema of a Cloud Spanner database as a list of formatted
        DDL statements. This method does not show pending schema updates, those may
        be queried using the Operations API.
      operationId: spanner.projects.instances.databases.getDdl
      x-api-path-slug: v1databaseddl-get
      parameters:
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Database Schema
    patch:
      summary: Update Database Schema
      description: |-
        Updates the schema of a Cloud Spanner database by
        creating/altering/dropping tables, columns, indexes, etc. The returned
        long-running operation will have a name of
        the format `<database_name>/operations/<operation_id>` and can be used to
        track execution of the schema change(s). The
        metadata field type is
        UpdateDatabaseDdlMetadata.  The operation has no response.
      operationId: spanner.projects.instances.databases.updateDdl
      x-api-path-slug: v1databaseddl-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Database Schema
  /v1/{database}/sessions:
    post:
      summary: Create Session
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
      operationId: spanner.projects.instances.databases.sessions.create
      x-api-path-slug: v1databasesessions-post
      parameters:
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Session
  /v1/{name}:
    delete:
      summary: End Session
      description: Ends a session, releasing server resources associated with it.
      operationId: spanner.projects.instances.databases.sessions.delete
      x-api-path-slug: v1name-delete
      parameters:
      - in: path
        name: name
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Session
    get:
      summary: Get Session
      description: |-
        Gets a session. Returns `NOT_FOUND` if the session does not exist.
        This is mainly useful for determining whether a session is still
        alive.
      operationId: spanner.projects.instances.databases.sessions.get
      x-api-path-slug: v1name-get
      parameters:
      - in: path
        name: name
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Session
    patch:
      summary: Update Instance
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
      operationId: spanner.projects.instances.patch
      x-api-path-slug: v1name-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Instance
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---