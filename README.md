Informal Description:

The Airline Reservation System comprises several interconnected classes designed to facilitate flight bookings and manage associated data. These classes include Airline, Flight, Passenger, Booking, Aircraft, and Crew.

Airline:

Description: Represents an airline company operating flights. It manages flight operations and passenger registrations.
Pre and Post Conditions: The pre-conditions for adding a flight include ensuring the flight parameter is not null. After adding a flight, it should be successfully added to the airline's list of flights.
Invariants: Every airline must have a unique code, must have at least one flight, and each flight associated with the airline must have a unique flight number.
Flight:

Description: Represents a scheduled flight with specific details such as flight number, origin, destination, and available seats. It allows passengers to book seats and cancels bookings if required.
Pre and Post Conditions: When booking a seat, the pre-condition ensures available seats exist and the passenger hasn't already booked the flight. Post-booking, the available seats decrease by one. Cancelling a booking requires a pre-existing booking, and upon cancellation, available seats increase by one.
Invariants: Each flight must have a unique flight number, non-negative available seats, and distinct origin and destination.
Passenger:

Description: Represents an individual who wishes to book a flight. It holds personal details and allows booking and cancelation of flights.
Pre and Post Conditions: When booking a flight, the pre-condition ensures available seats and no existing booking. Post-booking, the passenger successfully books the flight. Cancelling a flight requires a pre-existing booking, and upon cancellation, the booking is successfully canceled.
Invariants: Each passenger must have a unique passenger ID, a valid passport number, and can book only one seat per flight.
Booking:

Description: Represents a confirmed booking made by a passenger for a specific flight. It holds details such as booking ID, date, and seat number. It allows confirmation and cancellation of bookings.
Pre and Post Conditions: When confirming a booking, available seats must exist, and the booking must not be confirmed. Post-confirmation, a seat is assigned, and available seats decrease by one. Cancelling a booking requires a pre-existing confirmed booking, and upon cancellation, the booking is canceled, and available seats increase by one.
Invariants: Each booking must have a unique booking ID, must be associated with one flight and one passenger, and the seat number must be unique per flight.
Aircraft:

Description: Represents an aircraft used for flights. It holds details such as capacity and registration number and supports maintenance scheduling and capacity updates.
Pre and Post Conditions: When scheduling maintenance, there are no pre-conditions. Post-scheduling, maintenance is successfully scheduled. Updating capacity requires a non-negative new capacity, and upon updating, the capacity is successfully changed.
Invariants: The aircraft's capacity must be non-negative, must have a unique registration number, and maintenance scheduling cannot be null.
Crew:

Description: Represents a crew member involved in flight operations. It holds details such as crew ID, name, and position. It supports assignment to flights and position updates.
Pre and Post Conditions: When assigning to a flight, the pre-condition ensures the flight parameter is not null. Post-assignment, the crew member is successfully assigned to the flight. Updating position requires a non-null or empty new position, and upon updating, the position is successfully changed.
Invariants: Each crew member must have a unique crew ID, non-null name and position, and can only be assigned to one flight at a time.
These descriptions, along with the pre and post conditions and invariants, provide a comprehensive understanding of the behavior and constraints of each class within the Airline Reservation System.
