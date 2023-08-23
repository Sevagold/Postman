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

{
    "age": "24",
    "family": 
    {
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

    {
    "age": 24,
    "daily_food": 0.9,
    "daily_sleep": 187.5,
    "name": "Seva"
}

```

#### **REQUEST 4**
Method: GET
EndPoint: /object_info_2
request url params: 
 name: Seva
 age: 24
 salary: 1000
#### **Responce 4**
```sh
{
    "person": 
    {
        "u_age": 24,
        "u_name": [
            "Seva",
            1234,
            24
        ],
        "u_salary_5_years": 5182.8
    },
    "qa_salary_after_1.5_year": 4072.2,
    "qa_salary_after_12_months": 3331.8,
    "qa_salary_after_3.5_years": 4689.2,
    "qa_salary_after_6_months": 2468,
    "start_qa_salary": 1234
}
```

#### **REQUEST 5**
Method: GET
EndPoint: /object_info_3
request url params: 
 name: Seva
 age: 24
 salary: 1000
#### *Responce 5*
```sh
{
    "age": null,
    "family": 
    {
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
        "pets": 
        {
            "cat":
             {
                "age": 3,
                "name": "Sunny"
            },
            "dog":
             {
                "age": 4,
                "name": "Luky"
            }
        },
        "u_salary_1_5_year": 4000
    },
    "name": "Seva",
    "salary": 1000
}
```

#### **REQUEST 6**
Method: GET
EndPoint: /object_info_4
request url params: 
 name: Seva
 age: 24
 salary: 1000
#### *Responce 6*
```sh
{
    "age": 24,
    "name": "Seva",
    "salary": 
    [
        5000,
        "10000",
        "15000"
    ]
}

```

#### **REQUEST 7**
Method: POST
EndPoint: /user_info_2
request form data: 
 name: Seva
 age: 24
 salary: 1000
#### *Responce 7*
```sh
{
    "person": 
    {
        "u_age": 34,
        "u_name": [
            "Seva",
            1000,
            34
        ],
        "u_salary_5_years": 4200.0
    },
    "qa_salary_after_1.5_year": 3300.0,
    "qa_salary_after_12_months": 2700.0,
    "qa_salary_after_3.5_years": 3800.0,
    "qa_salary_after_6_months": 2000,
    "start_qa_salary": 1000
}
```










