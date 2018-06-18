---
swagger: "2.0"
x-collection-name: Stocklytics
x-complete: 1
info:
  title: Stocklytics Company Data API
  description: the-company-data-api-allows-you-to-retrieve-company-information-about-a-particular-stockticker-code-
  version: v1
host: api.stocklytics.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  companyData/{API_VERSION}/:
    get:
      summary: Company Data
      description: The Company Data API allows you to retrieve company information
        about a particular stock/ticker code.
      operationId: getCompanyData
      x-api-path-slug: companydataapi-version-get
      parameters:
      - in: query
        name: api_key
        description: Allows us to identify the request initiator
      - in: path
        name: API_VERSION
        description: Version of the API
      - in: query
        name: stock
        description: The stock code/ticker for the stock to look up
      responses:
        200:
          description: OK
      tags:
      - Companies
---