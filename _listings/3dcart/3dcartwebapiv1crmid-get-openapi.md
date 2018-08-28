---
swagger: "2.0"
x-collection-name: 3dcart
x-complete: 0
info:
  title: 3dcart Get a specific CRM
  version: 1.0.0
  description: Get a specific crm.
host: apirest.3dcart.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /3dCartWebAPI/v1/CRM:
    post:
      summary: Adds a new CRM to the system
      description: Adds a new crm to the system.
      operationId: CRM_PostCRM
      x-api-path-slug: 3dcartwebapiv1crm-post
      parameters:
      - in: body
        name: crm
        description: A Json or XML object containing the new CRM
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - S
      - New
      - CRM
      - To
      - System
  /3dCartWebAPI/v1/CRM/{crmid}/message:
    get:
      summary: Get all the messages from a specific CRM
      description: Get all the messages from a specific crm.
      operationId: CRM_GetAllCRMMessages
      x-api-path-slug: 3dcartwebapiv1crmcrmidmessage-get
      parameters:
      - in: path
        name: crmid
        description: CRM ID
      - in: query
        name: limit
        description: Maximum number of items that can be returned
      - in: query
        name: offset
        description: Starting point for the return data
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - Messages
      - From
      - Specific
      - CRM
  /3dCartWebAPI/v1/CRM/{crmid}/message/{msgid}:
    delete:
      summary: Delete a CRM Message in the system
      description: Delete a crm message in the system.
      operationId: CRM_DeleteCRM
      x-api-path-slug: 3dcartwebapiv1crmcrmidmessagemsgid-delete
      parameters:
      - in: path
        name: crmid
        description: CrmID
      - in: path
        name: msgid
        description: MessageID
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - CRM
      - Message
      - In
      - System
  /3dCartWebAPI/v1/CRM/{id}:
    get:
      summary: Get a specific CRM
      description: Get a specific crm.
      operationId: CRM_GetCRM
      x-api-path-slug: 3dcartwebapiv1crmid-get
      parameters:
      - in: path
        name: id
        description: CRM ID
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - Specific
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