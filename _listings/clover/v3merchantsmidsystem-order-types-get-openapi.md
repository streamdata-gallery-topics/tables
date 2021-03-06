---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Return a list of system order types
  version: 1.0.0
  description: Merchants can create custom Order Types via "/v3/merchants/{mId}/order_types".
    It is useful to associate these custom order types with particular system order
    types in order to group things functionally. For example, a merchant may have
    a "Lunch Take-Out" order type and a "Dinner Take-Out" order type. These two order
    types can be associated with the "TAKE-OUT-TYPE" system order type so that applications
    can understand that they are both take-out order types.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/sync/{table}:
    get:
      summary: Get a sync token (deprecated)
      description: Get a sync token (deprecated).
      operationId: GetSyncToken
      x-api-path-slug: v3merchantsmidsynctable-get
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: table
        description: Table Name
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Sync
      - Table
  /v3/merchants/{mId}/system_order_types:
    get:
      summary: Return a list of system order types
      description: Merchants can create custom Order Types via "/v3/merchants/{mId}/order_types".
        It is useful to associate these custom order types with particular system
        order types in order to group things functionally. For example, a merchant
        may have a "Lunch Take-Out" order type and a "Dinner Take-Out" order type.
        These two order types can be associated with the "TAKE-OUT-TYPE" system order
        type so that applications can understand that they are both take-out order
        types.
      operationId: GetSystemOrderTypes
      x-api-path-slug: v3merchantsmidsystem-order-types-get
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - System
      - Order
      - Types
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