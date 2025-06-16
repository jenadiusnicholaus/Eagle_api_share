# Case Witness
  - Fix attachment to attchments

All Attchment
  - Limit doc size to 5mb
  - added doc name(name) , in request payload, attachment_name

  Api change for attachment:
    1. Post: http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-exhibits/

    ```json
    {
  "pe": 1,
  "name": "RAV4",
  "exhibit_label_number": "ksksksooswssdssdsWW",
  "exhibit_description": "Description of the exhibit",
  "exhibit_type": 1,
  "exhibit_state": 2,
  "exhibit_status": 1,
  "exhibit_financial_value": 1000.00,
  "attachment": {
    "attachment_type": 3,
    "name": "eg_doc1",
    "attachment_path": "data:image/jpeg;base---"
  },
  "strong_room": 1,
  "strong_room_desc": "Top shelf, locked"

}
    ```
    

  
