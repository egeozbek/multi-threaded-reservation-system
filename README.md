# Multi-threaded Reservation System

A Multi-threaded Seat Reservation System that works on a NxM seating plan.

A Reservation request consists of the name of the person who makes the reservation and the id's of the seats that is to be reserved.

Eg. John A2 A0 A1

Upon a reservation request system simulates a database operation by sleeping for 50 ms. During this time period any reservation request on the seats already locked for database operation waits for the completion of the operation. This database operation has 10% chance of failing. After a successful or failed database operation any request that waits for completion resumes. If any of the awaited seats are successfully reserved by another user, thread exits with failure log, else it tried to reserve the prementioned seats


#### Keywords
```
multi-thread, concurrency, java, condition variable 
```

## Usage
```
git clone https://github.com/egeozbek/multi-threaded-reservation-system
cd multi-threaded-reservation-system/Source
javac *.java
java Main < ../Sample-IO/input.txt
```

Sample inputs located in ```Sample-IO``` folder can be used for testing purposes. 
