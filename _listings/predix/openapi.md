swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/accounts/{predix-zone-id}:
    post:
      summary: Create an EC system account
      description: Create a EC system account with the CF details
      operationId: create-a-ec-system-account-with-the-cf-details
      x-api-path-slug: adminaccountspredixzoneid-post
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: Cloud Foundry service instance details
      - in: body
        name: settings
        description: Cloud Foundry setting details
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - System
      - Account
    get:
      summary: Get the EC system account
      description: Get an existing EC system account by predix zone id
      operationId: get-an-existing-ec-system-account-by-predix-zone-id
      x-api-path-slug: adminaccountspredixzoneid-get
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: pass the predix zone id
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - System
      - Account
    delete:
      summary: Delete the EC system account
      description: Delete an existing EC system account by predix zone id
      operationId: delete-an-existing-ec-system-account-by-predix-zone-id
      x-api-path-slug: adminaccountspredixzoneid-delete
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: pass the predix zone id
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - System
      - Account