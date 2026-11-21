Project Title: KeettaKa, a GPS Route Finder Using a Graph and Dijkstra's Algorithm

Presented by: Group 5

KeettaKa is a simple GPS system that helps users find the shortest route between two places. Users can register, log in, search for a start and a destination, and see the route on a map page.

The program uses two main things. The first is a graph, where each place is a node and each road is an edge with a distance in km. The second is Dijkstra's algorithm, which checks the roads in the graph one by one and finds the shortest path from the start to the destination.

Phase 1: Register, Login, and Main Menu

The user opens the program and chooses Register, Login, or Exit.
When registering, the user enters a name and password. The system makes a unique 4-digit user ID and saves the account in accounts.txt.
To log in, the user enters the user ID and password. The system checks them against the saved accounts.
After logging in, the user goes to the main menu: Find Shortest Route, View Locations, Add a New Road, View Best Routes, or Logout.

Phase 2: Adding a New Road

The user chooses 2 points.
The system shows the list of locations. The user enters the IDs of the two places to connect.
If both IDs are valid, the system computes the distance from their coordinates and adds the road to the graph.
The program goes back to the main menu.

Phase 3: Finding the Shortest Route

The user chooses Find Shortest Route and the list of locations is displayed.
The user enters the ID of the starting place and the ID of the destination. If one of them is not found, the program goes back to the menu.
Dijkstra's algorithm runs on the graph and finds the shortest path and the total distance in km. If the two places are not connected, the system says that no route was found.
The system compares the result with the saved best route for this start and destination:
If there is no saved route yet, the new one is saved with the user's ID.
If the new route is shorter, the saved one is updated with the new distance, path, and user.
If it is not shorter, the saved route stays.
The system makes map.html, which draws the path on the map with markers for the start and the destination.
The program goes back to the main menu, where the user can search again or log out.

Phase 4: Viewing the Best Routes

The user chooses View Best Routes.
The system displays each saved route: the start, the destination, the shortest distance, the path, and the name of the user who found it.
If there are no saved routes yet, the system says so.
The program goes back to the main menu.
