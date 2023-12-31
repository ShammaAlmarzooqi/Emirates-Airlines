# Emirates-Airlines Routes
#### Video Demo:  <https://youtu.be/RcDeHPhYBBk?si=4nAQ7a3DuNmFLe2V>
#### Description:
Emirates Airlines Algorithm 
Get Flight Routes 
Initialize an empty list routes. 
Continuously prompt the user to enter a route. 
If the user enters "quit": 
Check if the number of routes is less than 10. 
If yes, inform the user that at least 10 routes are needed and continue prompting. If no, exit the loop and return the routes list. 
If the user enters a route, add it to the routes list. 
Get Route Prices 
Initialize an empty list prices. 
Iterate over each route in flight_routes. 
For each route, prompt the user to enter the price. 
Add the entered price to the prices list.
Return the prices list. 
Get Flight Seats 
Initialize an empty list seats. 
Iterate over each route in flight_routes. 
For each route, prompt the user to enter the number of seats. 
Add the entered number of seats to the seats list. 
Return the seats list. 
Get Route Ratings 
Initialize an empty list ratings. 
Iterate over each route in flight_routes. 
Continuously prompt the user to enter a rating between 1 and 5. 
Validate the entered rating (must be between 1 and 5). 
If valid, add the rating to the ratings list and move to the next route. 
If invalid, inform the user and prompt again. 
Return the ratings list. 
Display Route Information 
Print column headers for Route, Price, Seats, and Rating. 
Iterate over each route in flight_routes. 
For each route, print its corresponding price, number of seats, and rating in a formatted manner. 
Analyze Data to Get Specific Information 
Initialize four empty lists for storing popular routes, expensive routes, routes with few seats, and unique destinations. 
Iterate over each route in flight_routes. 
If the rating is greater than 3, add the route to popular_routes. 
If the price is greater than 500, add the route to expensive_routes. 
If the number of seats is less than 10, add the route to few_seats. 
If the route is not already in unique_destinations, add it. 
Return the lists popular_routes, expensive_routes, few_seats, and unique_destinations. Main Program Flow 
Call getFlightRoutes() and store the returned list in flight_routes. 
Call getRoutePrices() with flight_routes and store the returned list in route_prices. 
Call getFlightSeats() with flight_routes and store the returned list in route_seats. 
Call getRouteRatings() with flight_routes and store the returned list in route_ratings. Call displayRouteInformation() with flight_routes, route_prices, route_seats, and route_ratings. Call getData() with flight_routes, route_prices, route_seats, and route_ratings, and store the returned data in popular_routes, expensive_routes, few_seats, and unique_destinations. 
Display the analysis results for popular routes, expensive routes, routes with few seats, and unique destinations. 
