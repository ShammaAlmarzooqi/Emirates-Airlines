

In [ ]:# A function to get Flight Routes from user input 
def getFlightRoutes(): 
 # Initialize an empty tuple for storing routes 
 routes = () 
  
 while True: 
 # Prompt user for input 
 route = input("Please enter a route: ") 
  
 # Check if user wants to quit the input loop 
 if route.lower() == "quit": 
 # Ensure at least 10 routes are entered 
 if len(routes) < 10: 
 print("You must enter at least 10 routes") 
 continue 
 else: 
 # Return the tuple of routes 
 return routes 
 else: 
 # Add the new route to the tuple 
 routes += (route,) 
# A function to get prices for each route 
def getRoutePrices(flight_routes): 
 # Initialize an empty tuple for storing prices 
 prices = () 
 for i in range(len(flight_routes)): 
 # Prompt for the price of each route 
 print("Enter Price for flight " + str(i + 1) + ": ", end='')  price = int(input()) 
 # Add the price to the tuple 
 prices += (price,) 
 return prices 
# A function to get the number of seats for each flight 
def getFlightSeats(flight_routes): 
 # Initialize an empty tuple for storing seats 
 seats = () 
 for i in range(len(flight_routes)): 
 # Prompt for the number of seats for each flight 
 print("Enter total seats for flight " + str(i + 1) + ": ", end=' ')  seat = int(input()) 
 # Add the seat count to the tuple 
 seats += (seat,) 
 return seats 
# A function to get user ratings for each route 
def getRouteRatings(flight_routes): 
 # Initialize an empty tuple for storing ratings 
 ratings = () 
  
 for route in flight_routes: 
 while True: 
 try: 
 # Prompt for rating and ensure it's between 1 and 5  rating = float(input("Enter rating for " + route + " (1-5): "))   
 if 1 <= rating <= 5: 
 # Add valid rating to the tuple 
ratings += (rating,) 
 break 
 else: 
 print("Rating must be between 1 and 5.")
 except ValueError: 
 # Handle invalid numeric input 
 print("Invalid input. Please enter a numeric value.")   
 return ratings 
# A function to display all collected route information 
def displayRouteInformation(flight_routes, route_prices, route_seats, route_ratings):  # Print the header for the information table 
 print("Route".ljust(15) + "Price".rjust(15) + "Seats".rjust(15) + "Rating".rjust(15)   
 # Iterate over all routes to display their information 
 for i in range(len(flight_routes)): 
 print(flight_routes[i].ljust(15) + str(route_prices[i]).rjust(15) + str(route_se 
# A function to analyze and categorize routes based on certain criteria def getData(flight_routes, route_prices, route_seats, route_ratings):  # Initialize tuples for different categories of routes 
 popular_routes = () 
 expensive_routes = () 
 few_seats = () 
 unique_destinations = () 
  
 for i in range(len(flight_routes)): 
 # Categorize routes based on ratings, prices, seats, and uniqueness  if route_ratings[i] > 3: 
 popular_routes += (flight_routes[i],) 
  
 if route_prices[i] > 500: 
 expensive_routes += (flight_routes[i],) 
  
 if route_seats[i] < 10: 
 few_seats += (flight_routes[i],) 
  
 if flight_routes[i] not in unique_destinations: 
 unique_destinations += (flight_routes[i],) 
  
 return popular_routes, expensive_routes, few_seats, unique_destinations 
# Main execution block 
# Get all routes from the user 
flight_routes = getFlightRoutes() 
print() 
# Get prices for each route 
route_prices = getRoutePrices(flight_routes) 
print() 
# Get seat counts for each flight 
route_seats = getFlightSeats(flight_routes) 
print() 
# Get ratings for each route 
route_ratings = getRouteRatings(flight_routes) 
print() 
# Display all gathered information about routes 
displayRouteInformation(flight_routes, route_prices, route_seats, route_ratings) print() 
# Analyze the collected data to categorize routes 
popular_routes, expensive_routes, few_seats, unique_destinations = getData(flight_routes 
# Print the analysis results 
print("\nPopular Routes:", popular_routes) 
print("Expensive Routes:", expensive_routes)
print("Few Seats", few_seats) 
print("Unique Destinations", unique_destinations) 

