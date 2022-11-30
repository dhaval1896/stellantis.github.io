---
section: mobile-sdk
categorie: API Reference
layout: api-reference
version:
  available-since: 2.0
name: pims.authentication.smscode
subname: enrollment
domain: authentication
type: 
    - set
paramsset:
- name: action
  required: true
  description: Name of the action to perform, in this case *Enrollment*. 
  type: String
  unit-value: 
    - 'enrollment: enroll device'
  example: enrollment
- name: smsCode
  required: true
  description: SMS code value. See **GET pims.authentication.smscode - enrollment**.
  type: int
  unit-value: n/a
  example: " " #TODO
dataset: 
  - name: status
    description: Status of the action.
    type: String
    unit-value:
      - NotEnrolled
      - AlreadyEnrolled
    example: AlreadyEnrolled
errorset: 
  - code: 2001
  - code: 2006
  - code: 2102
  - code: 2201
  - code: 2202
  - code: 2204
  - code: 2308
  - code: 2309
  - code: 2310
  - code: 2311
  - code: 2312
  - code: 2313
  - code: 2314
  - code: 2316
  - code: 2317
  - code: 2344
short: |-
  This api allows to perform the first steps of device enrollment, next step is **pims.authentication.enrollment - enroll**.
textset: |-
  **SET** will send the SMS code received on the user trusted phone number for validation.
  
  The SMS is received using **GET pims.authentication.smscode**.
component: 
  - StrongAuthentication
---