swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
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
    get:
      summary: Get a single grading period
      description: Get a single grading period.
      operationId: get-a-single-grading-period
      x-api-path-slug: coursescourse-idgrading-periodsid-get
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
    put:
      summary: Update a single grading period
      description: Update a single grading period.
      operationId: update-a-single-grading-period
      x-api-path-slug: coursescourse-idgrading-periodsid-put
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
      - Id
  /courses/{course_id}/grading_standards:
    get:
      summary: List the grading standards available in a context.
      description: List the grading standards available in a context..
      operationId: list-the-grading-standards-available-in-a-context
      x-api-path-slug: coursescourse-idgrading-standards-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Grading
      - Standards
    post:
      summary: Create a new grading standard
      description: Create a new grading standard.
      operationId: create-a-new-grading-standard
      x-api-path-slug: coursescourse-idgrading-standards-post
      parameters:
      - in: query
        name: grading_scheme_entry[][name]
        description: The name for an entry value within a GradingStandard that describes
          thenrange of the value e
      - in: query
        name: grading_scheme_entry[][value]
        description: The value for the name of the entry within a GradingStandard
      - in: query
        name: title
        description: The title for the Grading Standard
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Grading
      - Standards