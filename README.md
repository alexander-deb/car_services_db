
## Логическая модель
![image](https://user-images.githubusercontent.com/50020386/161616308-8bb10543-48c8-4d69-8e84-e6e419f5e54c.png)


## Физическая модель
**CarService Автосервисы**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
sevice_ID |ID автосервиса  |  INT | NOT NULL|
address  | Адресс | VATCHAR(100) | NOT NULL|
phone_number |Телефон  | VARCHAR(12) | NOT NULL|
company_name |Наименование компании  | VARCHAR(50) | NOT NULL|


**Places Помещения**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
address  | Адресс | VATCHAR(100) | NOT NULL|
sevice_ID |ID автосервиса  |  INT | NOT NULL|
square |Площадь(м^2)  | INT | NOT NULL|
rent_price |Цена аренды(руб/мес)  | INT | NOT NULL|


**Employees Сотрудники**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
employee_ID  | ID сотрудника | INT | NOT NULL|
full_name |ФИО  |  VARCHAR(50) | NOT NULL|
sevice_ID |ID Автосервиса-работодателя  | INT | NOT NULL|
phone_number |Контактный телефон сотрудника  | VARCHAR(12) | NOT NULL|
passport_number |Паспортные данные  | VARCHAR(50) | NOT NULL|


**Orders Заказы**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
order_ID  | ID заказа | INT | NOT NULL|
employee_ID  | ID сотрудника, взявшего заказ | INT | NOT NULL|
serial_number_of_details |Серийный номер заказанной детали  |  VARCHAR(50) | NOT NULL|
sevice_ID |ID Автосервиса-выполняющего  | INT | NOT NULL|
price_of_job |Цена работ(руб)  | INT | NOT NULL|


**Clients Клиенты**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
client_ID  | ID клиента | INT | NOT NULL|
order_ID  | ID заказа | INT | NOT NULL|
full_name  | ФИО клиента | VARCHAR(50) | NOT NULL|

**Components Детали**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
serial_number  | Серийный номер детали | VARCHAR(50) | NOT NULL|
order_ID  | ID заказа | INT | NOT NULL|
price |Цена детали  |  INT | NOT NULL|
manufacturer | Производитель | VARCHAR(100) | NOT NULL|
provider_adress | Адрес поставщика  | VARCHAR(100) | NOT NULL|


**Providers Поставщики**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
address  | Серийный номер детали | VARCHAR(50) | NOT NULL|
service_ID  | ID сервиса, с которым заключен контракт | INT | NOT NULL|
company_name | Название компании-поставщика  |  VARCHAR(50) | NOT NULL|
city | Город поставщика | VARCHAR(50) | NOT NULL|

**Equipment Оборудование**
Название |Описание | Тип данных | Ограничение|
------ | ------|------|------|
serial_number  | Серийный номер | VARCHAR(100) | NOT NULL|
provider_address  | Адрес поставщика | VARCHAR(100) | NOT NULL|
service_ID | ID Автосервиса  |  INT | NOT NULL|
country_of_manufacturer | Страна производителя | VARCHAR(50) | NOT NULL|
company_name | Название компании-поставщика  |  VARCHAR(50) | NOT NULL|
price | Цена(руб) | INT | NOT NULL|



