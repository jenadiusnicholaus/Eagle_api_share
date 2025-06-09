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
# pe-exhibits
> GET:
> 
  http://127.0.0.1:8008/eagle/api/v1.0/core/pe/pe-suspects/?suspect_id=5&search=ID123456789&page=1&page_size=2

  You can search by either of the following fields
  ```json
  search_fields = [
        "exhibit_label_number",
        "name",
        "exhibit_description",
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





  
