{
  "info": {
    "name": "Google Cloud Spanner API Get Database Schema",
    "_postman_id": "078a3da1-76de-4c29-85de-533e3470c25b",
    "description": "Returns the schema of a Cloud Spanner database as a list of formatted\nDDL statements. This method does not show pending schema updates, those may\nbe queried using the Operations API.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "database schema",
      "item": [
        {
          "id": "ad71fd16-e39f-4e98-8544-ae4357b273ae",
          "name": "spanner.projects.instances.databases.getDdl",
          "request": {
            "url": {
              "protocol": "http",
              "host": "spanner.googleapis.com",
              "path": [
                "v1/:database/ddl"
              ],
              "variable": [
                {
                  "id": "database",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the schema of a Cloud Spanner database as a list of formatted\nDDL statements"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e134cc21-1540-409a-a424-8a0970437bf4"
            }
          ]
        }
      ]
    }
  ]
}