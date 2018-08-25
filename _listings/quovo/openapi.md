---
swagger: "2.0"
x-collection-name: Quovo
x-complete: 1
info:
  title: Quovo API v3
  description: todo-add-description
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
---