# UML - Запись к врачу через мобильное приложение:
```mermaid
classDiagram
class Hotel {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Room {
  +Int RoomNumber
  +String Type
  +Boolean Availability
  +Decimal Price
}

class Guest {
  +String Name
  +String Phone
  +String Address
}

class Booking {
  +Int ID
  +Guest Guest
  +Room Room
  +String PaymentMethod
  +String Status
  +DateTime CheckInDate
  +DateTime CheckOutDate
}

class RoomType {
  +String Type
  +Decimal Price
}

RoomType <|-- Room
Hotel <|-- Room
Guest <|-- Booking
Booking ..> Room
```
# UML - Заказ такси через мобильое приложение:
```mermaid
classDiagram
class TaxiCompany {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Driver {
  +String Name
  +String Phone
  +String CarModel
  +String CarNumber
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Ride {
  +Int ID
  +Customer Customer
  +Driver Driver
  +String PickupLocation
  +String DropoffLocation
  +Decimal Fare
  +String PaymentMethod
  +String Status
  +DateTime RequestTime
  +DateTime PickupTime
  +DateTime DropoffTime
}

class CarType {
  +String Type
  +Decimal BaseFare
  +Decimal PerKmFare
}

Driver <|-- CarType
TaxiCompany <|-- Driver
Customer <|-- Ride
Ride ..> Driver
```
# UML - Запись к врачу через мобильное приложение:
```mermaid
classDiagram
class MedicalCenter {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Doctor {
  +String Name
  +String Specialization
  +String Schedule
}

class Patient {
  +String Name
  +String Phone
  +String Address
}

class Appointment {
  +Int ID
  +Patient Patient
  +Doctor Doctor
  +DateTime AppointmentDate
  +String Status
}

class AppointmentType {
  +String Type
  +Decimal Price
}

Doctor <|-- AppointmentType
MedicalCenter <|-- Doctor
Patient <|-- Appointment
Appointment ..> Doctor
```
# UML - Покупка тура в турагенстве:
```mermaid
classDiagram
class TravelAgency {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Tour {
  +String Destination
  +DateTime DepartureDate
  +DateTime ReturnDate
  +Decimal Price
  +String Description
  +String ImageUrl
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Booking {
  +Int ID
  +Customer Customer
  +Tour Tour
  +String PaymentMethod
  +String Status
  +DateTime BookingDate
}

class TourOption {
  +Int ID
  +Tour Tour
  +String OptionName
  +Decimal OptionPrice
}

TourOption .. Tour
Booking .. Customer
Booking ..> TourOption
TravelAgency <|-- Tour
Customer <|-- Booking
Booking <|-- TourOption
```
# UML - Создание сайта автомагазина
```mermaid
classDiagram
class AutomobileStore {
  +String Name
  +String Address
  +String Phone
  +String Website
}

class Car {
  +String Make
  +String Model
  +Int Year
  +Decimal Price
  +String Description
  +String ImageUrl
}

class Customer {
  +String Name
  +String Phone
  +String Address
}

class Order {
  +Int ID
  +Customer Customer
  +Car Car
  +String PaymentMethod
  +String Status
  +DateTime OrderDate
}

class OrderItem {
  +Int ID
  +Car Car
  +Int Quantity
}

OrderItem .. Car
Order .. Customer
Order ..> OrderItem
AutomobileStore <|-- Car
Customer <|-- Order
Order <|-- OrderItem
```
