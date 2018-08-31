{
  "info": {
    "name": "Google Cloud Spanner API Delete Database",
    "_postman_id": "6ba994ee-453b-4dfc-bdaa-85eb3390682a",
    "description": "Drops (aka deletes) a Cloud Spanner database.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "database",
      "item": [
        {
          "id": "43ccb92c-2abc-43be-b946-42793c881eef",
          "name": "spanner.projects.instances.databases.dropDatabase",
          "request": {
            "url": {
              "protocol": "http",
              "host": "spanner.googleapis.com",
              "path": [
                "v1/:database"
              ],
              "variable": [
                {
                  "id": "database",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Drops (aka deletes) a Cloud Spanner database"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34826025-847c-4950-9e90-696f3e91a0db"
            }
          ]
        }
      ]
    }
  ]
}