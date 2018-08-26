---
swagger: "2.0"
x-collection-name: SalesLoft
x-complete: 1
info:
  title: SalesLoft
  description: salesloft-helps-transform-sales-teams-into-modern-sales-organizations---converting-more-target-accounts-into-customer-accounts
  version: v2
host: api.salesloft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/crm_activities.json:
    get:
      summary: List crm activities
      description: |-
        Fetches multiple crm activity records. The records can be filtered, paged, and sorted according to
        the respective parameters.
      operationId: v2.crm_activities.json.get
      x-api-path-slug: v2crm-activities-json-get
      parameters:
      - in: query
        name: ids
        description: IDs of crm activities to fetch
      - in: query
        name: include_paging_counts
        description: Whether to include total_pages and total_count in the metadata
      - in: query
        name: page
        description: The current page to fetch results from
      - in: query
        name: per_page
        description: How many records to show per page in the range [1, 100]
      - in: query
        name: sort_by
        description: 'Key to sort on, must be one of: created_at, updated_at'
      - in: query
        name: sort_direction
        description: 'Direction to sort in, must be one of: ASC, DESC'
      - in: query
        name: updated_at
        description: Equality filters that are applied to the updated_at field
      responses:
        200:
          description: OK
      tags:
      - Sales
      - List
      - Crm
      - Activities
  /v2/crm_activities/{id}.json:
    get:
      summary: Fetch a crm activity
      description: Fetches a crm activity, by ID only.
      operationId: v2.crm_activities.id.json.get
      x-api-path-slug: v2crm-activitiesid-json-get
      parameters:
      - in: path
        name: id
        description: Crm activity ID
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Fetch
      - Crm
      - Activity
---