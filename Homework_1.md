# POSTMAN
## _HOMEWORK 1, GET & POST_

- Protocol: http
- IP: 162.55.220.72
- Port: 5005

##### **REQUEST 1** 
Method: GET
EndPoint: /get_method
request url params: 
 name: Seva
 age: 24
 #### **Responce 1**
 ```sh
 [
    "Seva",
    "24"
]
```

#### **REQUEST 2**
Method: POST
EndPoint: /user_info_3
request form data: 
 name: Seva
 age: 24
 salary: 1000
 #### **Responce 1**
 ```sh
  [
{
    "age": "24",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "u_salary_1_5_year": 4000
    },
    "name": "Seva",
    "salary": 1000
}
]
```

#### **REQUEST 3**
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int
#### **Responce 3**
```sh
[
    {
    "age": 24,
    "daily_food": 0.9,
    "daily_sleep": 187.5,
    "name": "Seva"
}
]
```


