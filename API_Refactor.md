# Case Witness
  - Fix attachment to attchments

All Attchment
  - Limit doc size to 5mb
  - added doc name(name) , in request payload, attachment_name

  Api change for attachment:
 > POST:
 > PATCH:http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-exhibits/

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
    + "name": "eg_doc1",
    "attachment_path": "data:image/jpeg;base---"
  },
  "strong_room": 1,
  "strong_room_desc": "Top shelf, locked"

}
```
> POST PATCH, http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-attachments/
```json
{
  "name":"doc1",
  "attachment_path": "data:@file/pdf;base64..",
 + "attachment_type_id": 1,
  "pe": 1
}
```
>POST , PATCH http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-witnesses/
>
```json


{
    "pe_id": 1,
    "first_name": "Jenadius kss",
    "middle_name": "Michael",
    "last_name": "Doe",
    "identity_type_id": 1,
    "identification_number": "ID123456789",
    "phone_number": "+1234567890",
    "email": "john.doe@example.com",
    "sex_id": "1",
    "tribe_id": "2",
    "religion_id": "3",
    "dob": "1990-01-01",
    "submission_date": "2023-10-05",
    "pe": "12345",
    "occupation": "Software Engineer",
    "relationship": "Friend",
    "statement": "John Doe was seen at the scene of the incident.",
    "status": "active",
    "nationality_id": 1,
    "attachment_path": "data:image/jpeg;ba--",
    "attachment_type_id": 1,
    + "attachment_name": "enter_name here"
}

```
> POST http://127.0.0.1:8008/eagle/api/v1.0/core/create_confirmatory_test/
>
```json
{
    "exhibit": 18,
    "confirmatory_test_name": "Chemical Analysis Test",
    "confirmatory_test_desc": "Laboratory confirmation of substance composition",
    "confirmatory_test_date_conducted": "2023-11-15",
    "confirmatory_test_results": "Positive",
    "confirmatory_test_remarks": "Sample meets threshold requirements",
    "confirmatory_test_serial_number": "CT-2023-5678",
    "drug_type": 1,
    "attachment": "data:image/png;base64,iVBORw0K.....",
       
    + "attachment_name": "kakakaka"
    
}
```

> POST, PATCH  http://localhost:8008/eagle/api/v1.0/core/create_doc_preliminary_test/
```json
// http://localhost:8008/eagle/api/v1.0/core/create_doc_preliminary_test/
{
    "exhibit": 1,
    "sample_id": "Preliminary Test Name",
    "preliminary_test_desc": "Description of Preliminary Test",
    "preliminary_test_date_conducted": "2023-10-01",
    "preliminary_test_results": 1,
    "instruments": [
       1
    ],
    "sample_type_id": 1,
    "sample_from_id": 1,
    "attachment": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAzFBMVEX///8VFRUZGRk2NjYbGxszMzMfHx8YGBg",
 
    "drug_type_id": 1,
    + "attachment_name": "doc1"
}
```
>POST, PATCH http://127.0.0.1:8008/eagle/api/v1.0/core/create_doc_witness_info/
>
```json
{
    "witness_first_name": "John",
    "witness_middle_name": "Michael",
    "witness_last_name": "Doe",
    "witness_other_name": "Johnny",
   "case_info_id": 1,
    "witness_sex": 1,  
    "witness_dob": "1985-05-15",
    "witness_tribe": 1,  
    "witness_nationality": 1, 
    "witness_religion": 1,  
    "witness_identity_type": 1, 
    "witness_identity_number": "A1234567",
    "witness_phone_number": "+1234567890",
    "witness_email": "john.doe@example.com",
    "witness_occupation": "Software Developer",
    "witness_physical_address": "123 Main St, City",
    "witness_remarks": "Important witness in the case",
   
    "attachments": [
        {
        + "name": "security doc1",
        "attachment_type_id": 1,
        "attachment_path": "data:@file/pdf;base64,"
        }
    ]  
   
}

```

> ON Case, Exhibit POST and PATCH
>
```json
  # add
"attachments": [
        {
        + "name": "security doc1",
        "attachment_type_id": 1,
        "attachment_path": "data:@file/pdf;base64,"
        }
    ]
```


    

  
