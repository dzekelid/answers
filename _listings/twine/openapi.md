---
swagger: "2.0"
x-collection-name: Twine
x-complete: 1
info:
  title: Twine
  description: -overviewthe-twine-health-api-is-restful-api--the-requests-and-responses-are-formated-according-to-the-json-apihttpjsonapi-orgformat1-0-specification-in-addition-to-this-documentation-we-also-provide-an-openapihttpsgithub-comoaiopenapispecificationblobmasterversions2-0-md-yaml-file-describing-the-api-twine-api-specificationswagger-yaml--authenticationauthentication-for-the-twine-api-is-based-on-the-oauth-2-0-authorization-frameworkhttpstools-ietf-orghtmlrfc6749--twine-currently-supports-grant-types-of-client-credentials-and-refresh-token-see-post-oauthtokenoperationcreatetoken-for-details-on-the-request-and-response-formats--redocinject-securitydefinitions-
  version: 7.18.0
host: api.twinehealth.com
basePath: /pub
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /health_profile_answer:
    get:
      summary: List health profile answers
      description: Get a list of health profile answers
      operationId: fetchHealthProfileAnswers
      x-api-path-slug: health-profile-answer-get
      parameters:
      - in: query
        name: filter[groups]
        description: Comma-separated list of group ids
      - in: query
        name: filter[organization]
        description: Twine organization id
      - in: query
        name: filter[patient]
        description: Patient id to fetch healt profile answers
      - in: query
        name: include
        description: List of related resources to include in the response
      - in: query
        name: page[number]
        description: Page number
      - in: query
        name: page[size]
        description: Page size
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
      - Health
      - Profile
      - Answers
  /health_profile_answer/{id}:
    get:
      summary: Get a health profile answer
      description: Get a health profile answer by id
      operationId: fetchHealthProfileAnswer
      x-api-path-slug: health-profile-answerid-get
      parameters:
      - in: path
        name: id
        description: Health profile answer identifier
      - in: query
        name: include
        description: List of related resources to include in the response
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Health
      - Profile
      - Answer
---