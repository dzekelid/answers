---
swagger: "2.0"
x-collection-name: Quovo
x-complete: 0
info:
  title: Quovo Answer MFA challenges
  description: Answer available MFA Challenges for a connection.
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /connections/{connection_id}/challenges:
    put:
      summary: Answer MFA challenges
      description: Answer available MFA Challenges for a connection.
      operationId: ConnectionsChallengesByConnectionIdPut
      x-api-path-slug: connectionsconnection-idchallenges-put
      parameters:
      - in: path
        name: connection_id
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Answer
      - MFA
      - Challenges
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