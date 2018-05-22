{
  "info": {
    "name": "Google Cloud Spanner API Get Databases",
    "_postman_id": "a9d47bbd-2abf-4d4e-9a18-1c7619ac0e68",
    "description": "Lists Cloud Spanner databases.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "database",
      "item": [
        {
          "id": "4fff0891-2e78-4134-8588-9da50d4ad8f7",
          "name": "spanner.projects.instances.databases.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "spanner.googleapis.com",
              "path": [
                "v1/:parent/databases"
              ],
              "query": [
                {
                  "key": "pageSize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageToken",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "parent",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists Cloud Spanner databases"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e789b229-a916-43f0-8696-12b6ffc7b670"
            }
          ]
        }
      ]
    }
  ]
}