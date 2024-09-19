# BarberShop
This repository showcases a simple database structure for an imaginary barber shop, designed to demonstrate various database relationships.

Here's what you'll find:

Tables:

- barbers: Stores information about barbers, including ID, name, email, phone number, and hire date.
- clients: Stores information about clients, including ID, name, email, phone number, and join date.
- services: Stores information about offered services, including ID, name, description, duration, and price.
- appointments: Stores appointment details like ID, barber, client, service, date, time, and status.
- barber_services: Links barbers with services they offer (many-to-many relationship).

Relationships:

The database utilizes a combination of one-to-many and many-to-many relationships:

One-to-many:
- An appointment belongs to one barber (appointments.barber_id -> barbers.barber_id).
- An appointment belongs to one client (appointments.client_id -> clients.client_id).
- An appointment is for one service (appointments.service_id -> services.service_id).

Many-to-many: A barber can offer many services, and a service can be offered by many barbers (barber_services table with a composite primary key).
- The included DBML code defines the structure and relationships between tables.
