# Smart Elevator Control

This project presents the Entity Relationship Diagram (ERD) for a Smart Elevator Control Platform designed for large buildings such as malls, hospitals, airports, offices, and residential towers.


The system manages multiple buildings, elevators, floor requests, ride assignments, elevator status tracking, maintenance history, and ride logs for analytics.


The goal of this design is to support efficient elevator monitoring, request handling, and infrastructure management across multiple locations.

### System Features Supported

This database design supports:


- Managing multiple buildings on a single platform
- Tracking floors inside each building
- Managing multiple elevators per building
- Mapping elevators to the floors they serve
- Recording floor-level ride requests
- Assigning elevators to requests
- Tracking elevator movement status
- Logging ride history for analytics
- Monitoring maintenance activities
- Identifiying pending and completed requests
- Checking elevator availability
- Generating performance insights


### Entities Included in the ER Diagram

The following entities are used in the system:

1. Building
   
   Stores building-level information such as name, address, and location.
   
2. Floor
   
   Represents floors inside a building.
   
   Represents floors inside a building.
   
3. Elevator Shaft
   
   Represents shafts inside a building.
   
   Each shaft contains one elevator.
   
4. Elevator
   
   Stores elevator configuration details such as capacity, speed, and status availability.
   
   Each elevator belongs to one building and one shaft.
   
5. Elevator_Floor
   
   Acts as a junction table between elevators and floors.
   

   This allows:
   
   one elevator to serve multiple floors
   
   one floor to be served by multiple elevators
   
6. Floor_Request
   
   Stores ride requests generated from floors.
   

   Includes:
   

  - source floor
    
  - destination floor
    
  - direction (up/down)
    
  - request status
    
7. Ride_Assignment
   
  Tracks which elevator was assigned to a request.
  
  Helps monitor request handling flow.
  
8. Ride_Log
    
  Stores completed ride information for analytics.
  

  Includes:
  

  - start floor
    
  - destination floor
    
  - ride start time
    
  - ride end time
    
9. Elevator_Status
    
    Tracks real-time elevator condition such as:


  - idle
    
  - moving
    
  - maintenance
    
  - out of service
    
10. Maintenance


  Stores maintenance history for elevators.
  
  
  Includes issue details, duration, and maintenance status.
  

### Relationships Between Entities :Main relationships in the system:

- One building contains many floors
- One building contains many elevators
- One building contains many elevator shafts
- One elevator serves multiple floors
- One floor can be served by multiple elevators
- One floor generates many requests
- Each request is assigned to one elevator
- One elevator handles multiple ride requests
- One elevator has multiple status records
- One elevator has multiple maintenance records
- One request creates one ride log entry

### Design Highlights : This ER diagram follows good database design practices:

- Separates static configuration data from dynamic ride data
- Supports many-to-many relationships using junction tables
- Maintains maintenance history instead of overwriting data
- Tracks elevator status separately from ride logs
- Enables analytics using ride history
- Scalable for multiple buildings and elevators

### Use Cases Supported : Using this system, operations teams can:

- monitor elevator availability
- track pending ride requests
- check which elevator handled the most rides
- analyze ride frequency
- view maintenance history
- identify elevators under maintenance
- monitor real-time elevator movement

### Conclusion :
This ER diagram represents a scalable and real-world database structure for a smart elevator infrastructure monitoring system used in large commercial buildings.It ensures efficient request handling, elevator tracking, maintenance monitoring, and ride analytics across multiple buildings.
