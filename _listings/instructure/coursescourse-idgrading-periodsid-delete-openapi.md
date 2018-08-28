---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Delete a grading period
  description: Delete a grading period.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/grading_periods:
    get:
      summary: List grading periods
      description: List grading periods.
      operationId: list-grading-periods
      x-api-path-slug: coursescourse-idgrading-periods-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Grading
      - Periods
    post:
      summary: Create a single grading period
      description: Create a single grading period.
      operationId: create-a-single-grading-period
      x-api-path-slug: coursescourse-idgrading-periods-post
      parameters:
      - in: query
        name: grading_periods[][end_date]
        description: no description
      - in: query
        name: grading_periods[][start_date]
        description: The date the grading period starts
      - in: query
        name: grading_periods[][weight]
        description: The percentage weight of how much the period should count toward
          the coursengrade
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Grading
      - Periods
  /courses/{course_id}/grading_periods/id:
    delete:
      summary: Delete a grading period
      description: Delete a grading period.
      operationId: delete-a-grading-period
      x-api-path-slug: coursescourse-idgrading-periodsid-delete
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Grading
      - Periods
      - Id
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