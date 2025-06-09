# PE API

# Properties Case File(PE)
  > GET:
  http://127.0.0.1:8008/eagle/api/v1.0/core/case_properties/?case_infor_id=37&page=1&page_size=2

  > POST:
  http://127.0.0.1:8008/eagle/api/v1.0/core/create_case_property/
> 
  ### I just added the name
  
  ```json

    {
    "case_info": 1,
    "name": "sample name",
    "suspect_property_desc": "ksks",
    "suspect_property_remarks": "kssksk"
    }
```
# pe-suspects
> GET:
> 
  http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-suspects/?search=ID123456789&page=1&page_size=2

  You can search by either of the following fields
  ```python
   search_fields = [
        "external_user__first_name",
        "external_user__middle_name",
        "external_user__last_name",
        "external_user__identification_number",
    ]


```
  

>POST:
>
http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-suspects/
```json
{
    "pe_id": 1,
    "first_name": "jenadius Nicho",
    "middle_name": "Michael",
    "last_name": "Doe",
    "identification_number": "ID123456789",
    "phone_number": "+1234567890",
    "email": "john.doe@example.com",
    "sex_id": "1",
    "tribe_id": "2",
    "religion_id": "3",
    "nationality": "1",
    "identity_type_id": 1,
    "eye_color_id": 1,
    "hair_color_id": 1,
    "status": "active",
    "dob": "1990-01-01",
    "nationality_id": 214,
    "image": "data:image/jpeg;base64,/....."
}


```


> PATCH: 
  http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-suspects/?suspect_id=5
>

 ```json
{
    "pe_id": 1,
    "first_name": "jenadius Nicho",
    "middle_name": "Michael",
    "last_name": "Doe",
    "identification_number": "ID123456789",
    "phone_number": "+1234567890",
    "email": "john.doe@example.com",
    "sex_id": "1",
    "tribe_id": "2",
    "religion_id": "3",
    "nationality": "1",
    "identity_type_id": 1,
    "eye_color_id": 1,
    "hair_color_id": 1,
    "status": "active",
    "dob": "1990-01-01",
    "nationality_id": 214,
    "image": "data:image/jpeg;base64,/....."
}
 ```


# PE Witness
> GET:
 http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-witnesses/?search=Jenadius&page=1&page_size=2
>
> 
 search by 
 ```python
search_fields = [
        "external_user__first_name",
        "external_user__middle_name",
        "external_user__last_name",
        "external_user__identification_number",
        "external_user__phone_number",
        "external_user__email",
        "occupation",
        "relationship",
        "statement",
    ]
```

. POST:

 http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-witnesses/


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
    "attachment_path": "data:image/jpeg;base64,/9j/4A.....",
    "attachment_type_id": 1
}


```

> PATCH:
http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-witnesses/?witness_id=1
>
> Same json

#PE Exhibit

> GET:
http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-exhibits/?exhibit_id=2&search=RAV
>

search by

```json

  search_fields = [
        "exhibit_label_number",
        "name",
        "exhibit_description",
    ]
```

POST:

http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-exhibits/

```json
{
  "pe": 1,
  "name": "RAV4",
  "case_info": 2,
  "exhibit_label_number": "ksksksoosw",
  "exhibit_description": "Description of the exhibit",
  "exhibit_type": 1,
  "exhibit_state": 1,
  "exhibit_status": 1,
  "exhibit_financial_value": 1000.00,
  "attachment": {
    "attachment_type": 5,
    "attachment_path": "data:image/jpeg;base64,/9j/4..."
  },
  "strong_room": 1,
  "strong_room_desc": "Top shelf, locked",
  "created_by": 7
}
```

>PATCH:
>
>http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-exhibits/?exhibit_id=2
> same body

# PE Attachment

GET: http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-attachments/?attachment_id=2&search=attachment_type

POST, and PATCH
```json
{
  "attachment_path": "data:application/pdf;base64,JVBERi0xLjQKJcTl8uXrp/Og0MTGCjEgMCBvYmoKPDwvTGluZWFyaXplZCAxL0wgMTEzODQvTyAyL0UgMTA1MTIvTiAxL1QgMTEyNTg+PgplbmRvYmoK...", 
  "attachment_type_id": 1,
  "pe": 1         

}
```












  
