---
swagger: "2.0"
x-collection-name: Data2CRM
x-complete: 0
info:
  title: Data2CRM GET for Crm
  description: Return CRM information
  version: "1"
host: api.data2crm.com:80
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /crm:
    get:
      summary: GET for Crm
      description: Returns all CRMs from the system
      operationId: getCrmCollection
      x-api-path-slug: crm-get
      parameters:
      - in: query
        name: filter
        description: Filter
      - in: query
        name: limit
        description: 'Amount of results (default: 25)'
      - in: query
        name: offset
        description: 'Start from record (default: 0)'
      - in: query
        name: type
        description: Type
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - CRM
    post:
      summary: POST for Crm
      description: Add CRM into the systemWhat do I need to connect a CRM to Data2CRM.API?
      operationId: createCrmEntity
      x-api-path-slug: crm-post
      parameters:
      - in: body
        name: body
        description: Add CRM into the systemWhat do I need to connect a CRM to Data2CRM
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - CRM
  /crm/count:
    get:
      summary: COUNT for Crm
      description: Count all CRMs from the system
      operationId: getCrmCountCollection
      x-api-path-slug: crmcount-get
      parameters:
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - Crm
      - Count
  /crm/{crm_id}:
    delete:
      summary: DELETE for Crm
      description: Delete CRM information
      operationId: deleteCrmEntity
      x-api-path-slug: crmcrm-id-delete
      parameters:
      - in: path
        name: crm_id
        description: CRM Identifier
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - CRM
    get:
      summary: GET for Crm
      description: Return CRM information
      operationId: getCrmEntity
      x-api-path-slug: crmcrm-id-get
      parameters:
      - in: path
        name: crm_id
        description: CRM Identifier
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - CRM
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