---
section: mobile-sdk
categorie: API Reference
layout: api-reference
version:
  available-since: 2.0
name: pims.authentication.user
subname: updateLogin
domain: authentication
type:
  - set
params:
- name: action
  required: true
  type: String
  description: Name of the action to perform, in this case `updateLogin`. 
  unit-value: 
    - updateLogin
  example: updateLogin
- name: local
  description : Define the language to use in the external user agent (web view).
  type : string
  unit-value: #todo
  required: false 
  example: "en"
- ref: context
data: none
error: 
  - code: 2001
  - code: 2101
  - code: 2102
  - code: 2368
short: This api allows to update user login. It will prompt an external user agent (web view).
component:
  - BasicAuthentication
---