---
swagger: "2.0"
x-collection-name: Data2CRM
x-complete: 1
info:
  title: Data2CRM.API
  description: pmake-use-of-our-indepth-documentation-to-get-more-information-about-the-various-functions-of-the-service--those-willing-to-explore-the-mechanics-of-data2crm-api-can-test-it-in-live-regime-using-the-short-code-samples-ppselect-crm-span-iddocsselectcrm-stylefontweight-boldloading----please-waitspanpphere-are-the-api-access-keysbrbxapi2crmuserkeyb-span-iddocsuserkeye2a6379ab878ae7e58119d4ec842bf9c926e05b5spanbrbxapi2crmcrmkeyb-span-iddocscrmkey7ae5b17008fb414d84981191cf3b66a476ef8befspanpp-iddocscrmaccessthe-crm-access-details-arebrburlb-a-iddocscrmurl-hrefhttpslogin-salesforce-com-target-blankhttpslogin-salesforce-comabrbemail--usernameb-span-iddocscrmusernamedevelopers-data2crm-api1magneticone-comspanbrbpasswordb-span-iddocscrmpassworddata2crmapi123spanp
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
    put:
      summary: PUT for Crm
      description: Update CRM informationWhat do I need to connect a CRM to Data2CRM.API?
      operationId: updateCrmEntity
      x-api-path-slug: crmcrm-id-put
      parameters:
      - in: body
        name: body
        description: Update CRM informationWhat do I need to connect a CRM to Data2CRM
        schema:
          $ref: '#/definitions/holder'
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
---