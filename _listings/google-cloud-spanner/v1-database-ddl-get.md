---
swagger: "2.0"
info:
  title: Cloud Spanner
  description: Cloud Spanner is a managed, mission-critical, globally consistent and
    scalable relational database service.
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
  /v1/{database}/ddl:
    get:
      summary: Get Database Schema
      description: |-
        Returns the schema of a Cloud Spanner database as a list of formatted
        DDL statements
      operationId: spanner.projects.instances.databases.getDdl
      parameters:
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - database schema
definitions:
  AuditConfig:
    properties:
      auditLogConfigs:
        description: This is a default description.
        type: post
      exemptedMembers:
        description: This is a default description.
        type: post
      service:
        description: This is a default description.
        type: post
  AuditLogConfig:
    properties:
      exemptedMembers:
        description: This is a default description.
        type: post
      logType:
        description: This is a default description.
        type: post
  BeginTransactionRequest:
    properties: []
  Binding:
    properties:
      members:
        description: This is a default description.
        type: post
      role:
        description: This is a default description.
        type: post
  ChildLink:
    properties:
      childIndex:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      variable:
        description: This is a default description.
        type: post
  CloudAuditOptions:
    properties: []
  CommitRequest:
    properties:
      mutations:
        description: This is a default description.
        type: post
      transactionId:
        description: This is a default description.
        type: post
  CommitResponse:
    properties:
      commitTimestamp:
        description: This is a default description.
        type: post
  Condition:
    properties:
      iam:
        description: This is a default description.
        type: post
      op:
        description: This is a default description.
        type: post
      svc:
        description: This is a default description.
        type: post
      sys:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  CounterOptions:
    properties:
      field:
        description: This is a default description.
        type: post
      metric:
        description: This is a default description.
        type: post
  CreateDatabaseMetadata:
    properties:
      database:
        description: This is a default description.
        type: post
  CreateDatabaseRequest:
    properties:
      createStatement:
        description: This is a default description.
        type: post
      extraStatements:
        description: This is a default description.
        type: post
  CreateInstanceMetadata:
    properties:
      cancelTime:
        description: This is a default description.
        type: post
      endTime:
        description: This is a default description.
        type: post
      startTime:
        description: This is a default description.
        type: post
  CreateInstanceRequest:
    properties:
      instanceId:
        description: This is a default description.
        type: post
  DataAccessOptions:
    properties: []
  Database:
    properties:
      name:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
  Delete:
    properties:
      table:
        description: This is a default description.
        type: post
  Empty:
    properties: []
  ExecuteSqlRequest:
    properties:
      paramTypes:
        description: This is a default description.
        type: post
      params:
        description: This is a default description.
        type: post
      queryMode:
        description: This is a default description.
        type: post
      resumeToken:
        description: This is a default description.
        type: post
      sql:
        description: This is a default description.
        type: post
  Field:
    properties:
      name:
        description: This is a default description.
        type: post
  GetDatabaseDdlResponse:
    properties:
      statements:
        description: This is a default description.
        type: post
  GetIamPolicyRequest:
    properties: []
  Instance:
    properties:
      config:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      labels:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      nodeCount:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
  InstanceConfig:
    properties:
      displayName:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  KeyRange:
    properties:
      endClosed:
        description: This is a default description.
        type: post
      endOpen:
        description: This is a default description.
        type: post
      startClosed:
        description: This is a default description.
        type: post
      startOpen:
        description: This is a default description.
        type: post
  KeySet:
    properties:
      all:
        description: This is a default description.
        type: post
      keys:
        description: This is a default description.
        type: post
      ranges:
        description: This is a default description.
        type: post
  ListDatabasesResponse:
    properties:
      databases:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListInstanceConfigsResponse:
    properties:
      instanceConfigs:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListInstancesResponse:
    properties:
      instances:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListOperationsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      operations:
        description: This is a default description.
        type: post
  LogConfig:
    properties: []
  Mutation:
    properties: []
  Operation:
    properties:
      done:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      response:
        description: This is a default description.
        type: post
  PartialResultSet:
    properties:
      chunkedValue:
        description: This is a default description.
        type: post
      resumeToken:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  PlanNode:
    properties:
      childLinks:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      executionStats:
        description: This is a default description.
        type: post
      index:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
  Policy:
    properties:
      auditConfigs:
        description: This is a default description.
        type: post
      bindings:
        description: This is a default description.
        type: post
      etag:
        description: This is a default description.
        type: post
      iamOwned:
        description: This is a default description.
        type: post
      rules:
        description: This is a default description.
        type: post
      version:
        description: This is a default description.
        type: post
  QueryPlan:
    properties:
      planNodes:
        description: This is a default description.
        type: post
  ReadOnly:
    properties:
      exactStaleness:
        description: This is a default description.
        type: post
      maxStaleness:
        description: This is a default description.
        type: post
      minReadTimestamp:
        description: This is a default description.
        type: post
      readTimestamp:
        description: This is a default description.
        type: post
      returnReadTimestamp:
        description: This is a default description.
        type: post
      strong:
        description: This is a default description.
        type: post
  ReadRequest:
    properties:
      columns:
        description: This is a default description.
        type: post
      index:
        description: This is a default description.
        type: post
      limit:
        description: This is a default description.
        type: post
      resumeToken:
        description: This is a default description.
        type: post
      table:
        description: This is a default description.
        type: post
  ReadWrite:
    properties: []
  ResultSet:
    properties:
      rows:
        description: This is a default description.
        type: post
  ResultSetMetadata:
    properties: []
  ResultSetStats:
    properties:
      queryStats:
        description: This is a default description.
        type: post
  RollbackRequest:
    properties:
      transactionId:
        description: This is a default description.
        type: post
  Rule:
    properties:
      action:
        description: This is a default description.
        type: post
      conditions:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      in:
        description: This is a default description.
        type: post
      logConfig:
        description: This is a default description.
        type: post
      notIn:
        description: This is a default description.
        type: post
      permissions:
        description: This is a default description.
        type: post
  Session:
    properties:
      name:
        description: This is a default description.
        type: post
  SetIamPolicyRequest:
    properties:
      updateMask:
        description: This is a default description.
        type: post
  ShortRepresentation:
    properties:
      description:
        description: This is a default description.
        type: post
      subqueries:
        description: This is a default description.
        type: post
  Status:
    properties:
      code:
        description: This is a default description.
        type: post
      details:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
  StructType:
    properties:
      fields:
        description: This is a default description.
        type: post
  TestIamPermissionsRequest:
    properties:
      permissions:
        description: This is a default description.
        type: post
  TestIamPermissionsResponse:
    properties:
      permissions:
        description: This is a default description.
        type: post
  Transaction:
    properties:
      id:
        description: This is a default description.
        type: post
      readTimestamp:
        description: This is a default description.
        type: post
  TransactionOptions:
    properties: []
  TransactionSelector:
    properties:
      id:
        description: This is a default description.
        type: post
  Type:
    properties:
      code:
        description: This is a default description.
        type: post
  UpdateDatabaseDdlMetadata:
    properties:
      commitTimestamps:
        description: This is a default description.
        type: post
      database:
        description: This is a default description.
        type: post
      statements:
        description: This is a default description.
        type: post
  UpdateDatabaseDdlRequest:
    properties:
      operationId:
        description: This is a default description.
        type: post
      statements:
        description: This is a default description.
        type: post
  UpdateInstanceMetadata:
    properties:
      cancelTime:
        description: This is a default description.
        type: post
      endTime:
        description: This is a default description.
        type: post
      startTime:
        description: This is a default description.
        type: post
  UpdateInstanceRequest:
    properties:
      fieldMask:
        description: This is a default description.
        type: post
  Write:
    properties:
      columns:
        description: This is a default description.
        type: post
      table:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
x-collection-name: Google Cloud Spanner
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