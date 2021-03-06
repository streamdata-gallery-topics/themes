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
  /themes:
    get:
      summary: Get theme information for a tenant
      description: Get theme information
      operationId: getThemeUsingGET
      x-api-path-slug: themes-get
      responses:
        200:
          description: OK
      tags:
      - Themes
    post:
      summary: Save theme config information
      description: Save theme config information
      operationId: saveThemeUsingPOST
      x-api-path-slug: themes-post
      parameters:
      - in: body
        name: theme
        description: theme
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Themes
    put:
      summary: Update theme
      description: Update theme
      operationId: updateThemeUsingPUT
      x-api-path-slug: themes-put
      parameters:
      - in: body
        name: theme
        description: theme
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Themes
  /themes/{uuid}:
    get:
      summary: Get the registered theme by uri
      description: Get the registered theme infromation for the given uri
      operationId: getThemeInfoByIdUsingGET
      x-api-path-slug: themesuuid-get
      parameters:
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Themes
      - Uuid
    delete:
      summary: Delete theme
      description: Delete theme
      operationId: deleteThemeUsingDELETE
      x-api-path-slug: themesuuid-delete
      parameters:
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Themes
      - Uuid