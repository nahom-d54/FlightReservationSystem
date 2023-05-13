# FlightReservationSystem
# Usage Documentation for Flight Reservation System

## Introduction
The Flight Reservation System is a C++ command-line application that manages flight reservations. It allows users to add flights, list flights based on certain search criteria, reserve seats on flights, and cancel existing reservations. The program stores flight and reservation data in two separate text files: flights.txt and reservations.txt.

## Classes and Data Structures
- The Flight template class represents a flight with data members for the flight number, origin, destination, capacity, fare, seats available, departure time, arrival time, and a queue of reservations.
- The Reservation class represents a flight reservation with data members for the reservation number, flight number, passenger name, and seat number.
- The FlightReservationSystem class handles the loading and saving of flight and reservation data to and from text files. It also provides functions to add flights, list flights, reserve seats, and cancel reservations.

## Functions
- loadFlights() : Loads flight data from the flights.txt file and stores it in a vector and map.
- saveFlights() : Saves the flight data to the flights.txt file.
- loadReservations() Loads reservation data from the reservations.txt file and stores it in a queue and map.
- saveReservations() : Saves the reservation data to the reservations.txt file.
- tryWaitlist() : Processes reservations in the waitlist queue and tries to reserve seats for those reservations, if seats are available.
- addFlight(...) : Adds a new flight to the system.
- listFlights(...) : Lists flights based on specified search criteria.
- reserveSeat(...) : Reserves a seat on a flight for a passenger.
- cancelReservation(...) : Cancels an existing reservation.

## Usage Instructions
1. Compile the program using a C++ compiler.
2. Run the compiled executable.
3. The program will prompt you for commands. The available commands are:
- addflight <flight_number> <origin> <destination> <capacity> <departure_time> <arrival_time> : Adds a new flight to the system.
- listflights <origin> <destination> <departure_time> : Lists flights matching the given origin, destination, and departure time.
- reserveseat <flight_number> <passenger_name> : Reserves a seat on the specified flight for the given passenger.
- cancelreservation <reservation_number> : Cancels a reservation with the given reservation number.
- quit : Exits the program.
4. Enter commands as needed, following the syntax provided above.
5. To exit the program, enter the quit command.

## Examples
- Adding a flight:

 ```
 Enter command: addflight AA001 LAX JFK 200 10:00 18:00
  Flight AA001 added.
```  

- Listing flights:
```
 Enter command: listflights LAX JFK 08:00
  AA001, LAX to JFK, 10:00 - 18:00, 200 seats available.
  ```

- Reserving a seat:
```
 Enter command: reserveseat AA001 John Doe
  Reservation successful. Reservation number is 1.
  ```

- Canceling a reservation:
```
 Enter command: cancelreservation 1
  Reservation 1 cancelled.
  
```
