# Database Schema

## Table: customers

| Column     | Data Type         | Description               | Nullability  |
|------------|-------------------|--------------------------- |--------------|
| cid        | int               | Customer ID (Primary Key)  | NOT NULL     |
| cname      | varchar(50)       | Customer Name              | ALLOW NULL   |
| email      | varchar(50)       | Email Address              | ALLOW NULL   |
| phno       | char(10)          | Phone Number               | ALLOW NULL   |
| pin        | varchar(20)       | PIN Code                   | ALLOW NULL   |
| cadd       | varchar(250)      | Customer Address           | ALLOW NULL   |
| city       | varchar(50)       | City                        | ALLOW NULL   |
| password   | varchar(50)       | Password                   | ALLOW NULL   |
| dstat      | int               | Status                      | ALLOW NULL   |
| date_cr    | varchar(50)       | Creation Date              | ALLOW NULL   |

## Table: pets

| Column     | Data Type         | Description               | Nullability  |
|------------|-------------------|--------------------------- |--------------|
| pet_id     | int               | Pet ID (Primary Key)       | NOT NULL     |
| cid        | int               | Customer ID (Foreign Key referencing Customers) | ALLOW NULL |
| pet_name   | varchar(50)       | Pet Name                   | ALLOW NULL   |
| pet_age    | int               | Pet Age                    | ALLOW NULL   |
| pet_gen    | varchar(10)       | Pet Gender                 | ALLOW NULL   |
| pet_type   | varchar(50)       | Pet Type                   | ALLOW NULL   |
| dstat      | int               | Status                      | ALLOW NULL   |
| date_pr    | varchar(50)       | Date Purchased             | ALLOW NULL   |

## Table: company

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| adminid          | int               | Admin ID (Primary Key)     | ALLOW NULL   |
| city             | varchar(50)       | City                        | ALLOW NULL   |
| pincode          | varchar(6)        | Pincode                    | ALLOW NULL   |
| district         | varchar(50)       | District                   | ALLOW NULL   |
| companyaddress   | varchar(500)      | Company Address            | ALLOW NULL   |
| phoneno          | varchar(10)       | Phone Number               | ALLOW NULL   |
| email            | varchar(50)       | Email Address              | ALLOW NULL   |
| password         | varchar(50)       | Password                   | ALLOW NULL   |
| username         | varchar(50)       | Username                   | ALLOW NULL   |

## Table: groom

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| groomingid       | int               | Grooming ID (Primary Key)  | ALLOW NULL   |
| groomingname     | varchar(35)       | Grooming Name              | ALLOW NULL   |
| groomingdetails  | varchar(350)      | Grooming Details           | ALLOW NULL   |
| pet_type         | varchar(50)       | Pet Type                   | ALLOW NULL   |
| groomingcost     | int               | Grooming Cost              | ALLOW NULL   |
| dstat            | int               | Status                      | ALLOW NULL   |

## Table: pet_type

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| dstat            | int               | Status                      | ALLOW NULL   |
| pet_type         | varchar(50)       | Pet Type                   | ALLOW NULL   |
| typeid           | int               | Type ID (Primary Key)      | ALLOW NULL   |

## Table: news

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| dstat            | int               | Status                      | ALLOW NULL   |
| news             | varchar(500)      | News                        | ALLOW NULL   |
| nid              | int               | News ID (Primary Key)       | ALLOW NULL   |

## Table: request

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| rdate            | varchar(50)       | Request Date               | ALLOW NULL   |
| dstat            | int               | Status                      | ALLOW NULL   |
| rstat            | int               | Request Status             | ALLOW NULL   |
| rreply           | varchar(1000)     | Request Reply              | ALLOW NULL   |
| categ            | varchar(20)       | Category                    | ALLOW NULL   |
| rcontent         | varchar(1000)     | Request Content            | ALLOW NULL   |
| date             | varchar(50)       | Date                        | ALLOW NULL   |
| cname            | varchar(50)       | Customer Name              | ALLOW NULL   |
| cid              | int               | Customer ID (Foreign Key referencing Customers) | ALLOW NULL |
| rid              | int               | Request ID (Primary Key)   | ALLOW NULL   |

## Table: slot

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| slot             | varchar(25)       | Slot                        | ALLOW NULL   |
| sid              | int               | Slot ID (Primary Key)      | ALLOW NULL   |

## Table: booking

| Column           | Data Type         | Description               | Nullability  |
|------------------|-------------------|--------------------------- |--------------|
| bid              | int               | Booking ID (Primary Key)   | ALLOW NULL   |
| cid              | int               | Customer ID (Foreign Key referencing Customers) | ALLOW NULL |
| groomid          | int               | Groom ID (Foreign Key referencing Groom) | ALLOW NULL |
| slot             | varchar(50)       | Slot                        | ALLOW NULL  |
| groomingname     | varchar(50)       | Grooming Name              | ALLOW NULL  |
| app_date         | varchar(50)       | Appointment Date           | ALLOW NULL  |
| status           | int               | Status                      | ALLOW NULL  |
| book_date        | varchar(50)       | Booking Date               | ALLOW NULL  |
| rate             | int               | Rate                        | ALLOW NULL  |
| phono            | varchar(10)       | Phone Number               | ALLOW NULL  |
| cname            | varchar(50)       | Customer Name              | ALLOW NULL  |
| pet_id           | int               | Pet ID (Foreign Key referencing Pets) | ALLOW NULL |
| pet_name         | varchar(50)       | Pet Name                   | ALLOW NULL  |
| statdate         | varchar(50)       | Status Date                | ALLOW NULL  |
