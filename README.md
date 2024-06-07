# Flight Management System
Project Structure
The project consists of several main classes:

Aeropuerto (Airport)
Vuelo (Flight)
Pasajero (Passenger)
App
Additionally, the project includes two interfaces:

IPagable (Payable)
IReservable (Reservable)
Classes and Functionalities
Class Aeropuerto
Represents an airport and contains information about departing and arriving flights.

Attributes:

nombre (name): Name of the airport.
ubicacion (location): Location of the airport.
vuelosPartida (departingFlights): List of flights departing from the airport.
vuelosLlegada (arrivingFlights): List of flights arriving at the airport.
Methods:

registrarVueloPartida(Vuelo vuelo): Registers a departing flight.
registrarVueloLlegada(Vuelo vuelo): Registers an arriving flight.
Getter methods for the attributes.
Class Vuelo
Represents a flight and contains relevant information about the flight and the passengers.

Attributes:

numeroVuelo (flightNumber): Flight number.
aerolinea (airline): Name of the airline.
horaSalida (departureTime): Departure time of the flight.
destino (destination): Destination of the flight.
capacidadMaxima (maximumCapacity): Maximum passenger capacity.
aeropuertoPartida (departureAirport): Departure airport.
aeropuertoLlegada (arrivalAirport): Arrival airport.
pasajeros (passengers): List of passengers on the flight.
Methods:

reservarAsiento(int numeroAsiento): Reserves a seat on the flight.
agregarPasajero(Pasajero pasajero): Adds a passenger to the flight.
Getter methods for the attributes.
Class Pasajero
Represents a passenger and contains personal information and luggage details.

Attributes:

nombre (name): Name of the passenger.
numeroPasaporte (passportNumber): Passport number of the passenger.
cantidadEquipaje (luggageAmount): Amount of luggage of the passenger.
vuelosReservados (reservedFlights): List of flights reserved by the passenger.
Methods:

calcularPrecioReserva(): Calculates the reservation price based on the amount of luggage.
Getter methods for the attributes.
Class App
Contains the main method and functions to interact with the user and manage the system.

Methods:

registrarAeropuerto(ArrayList<Aeropuerto> aeropuertos, Scanner scanner): Registers a new airport.
reservarAsientosEnVuelo(ArrayList<Aeropuerto> aeropuertos, Scanner scanner): Reserves seats on a flight.
registrarVueloPartida(ArrayList<Aeropuerto> aeropuertos, Scanner scanner): Registers a departing flight.
registrarVueloLlegada(ArrayList<Aeropuerto> aeropuertos, Scanner scanner): Registers an arriving flight.
verCantidadPasajerosEnVuelo(ArrayList<Aeropuerto> aeropuertos, Scanner scanner): Shows the number of passengers on a flight.
Auxiliary methods to search for flights and airports.
Interfaces
IPagable (Payable)
Contains the calcularPrecioReserva() method that must be implemented by classes needing to calculate the reservation price.

IReservable (Reservable)
Contains the reservarAsiento(int numeroAsiento) method that must be implemented by classes that allow seat reservations.

How to Run the Project
Ensure you have Java installed on your system.
Compile the project using the following command:
bash
Copiar código
javac *.java
Run the main application:
bash
Copiar código
java App
Follow the on-screen instructions to interact with the system.
Main Menu Options
Register Airport: Allows registering a new airport.
Reserve seats on flight: Allows reserving seats on a flight by specifying the flight number and the number of seats.
Register departing flight: Allows registering a departing flight by specifying the flight details.
Register arriving flight: Allows registering an arriving flight by specifying the flight details.
View number of passengers on a flight: Shows the number of passengers on a flight by specifying the flight number.
Exit: Ends the program execution.
Considerations
Ensure to enter valid and consistent data to avoid errors in program execution.
The system does not store data in a database, so data will be lost upon program termination.
Thank you for using our Flight Management System!
