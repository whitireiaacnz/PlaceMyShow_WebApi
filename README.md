# PlaceMyShow_WebApi
REST API's for Place My Show App

Download This RAR file

Points Covered: 
1.Ability to view all the movies playing in your city
2.Ability to check all cinemas in which a movie is playing along with all the showtimes
3.User Sign up and login 
4.Ability to book a ticket.
5.The API to book a ticket should be protected i.e. only a logged-in user should be allowed to access that API. Rest, all other APIs are public endpoints
6.Use Dependency Injection

Additional Ponts
1.Have also used Auto mapper to map the the data transfer objects(DTO's)
2.Have followed the Repository Pattern.
3.Have mapped the roles and permissions.


PreRequisites : 

1.Aoutomapper for .NET Core
2.Entity Framework core
3.Identity
4.JWTBearer

Tasks Delivered

1. API Endpoint for getallmovies ---> /api/movies (returns all the movies)

2. API Endpoint to return all the  cinemas in which a movie is playing ----> /api/movies/{String Name} (returns all the objects in which the supplied movie is playing).

3. API Endpoint to SignUp ---> /api/Authenticate/Register {Body requires UserName,Email,Password } (For all the users without authorization)

4. API Endpoint to SignUp ---> /api/Authenticate/RegisterAdmin {Body requires UserName,Email,Password } (For admin)

5. API Endpoint to LogIn ----> /api/Authenticate/login {Body requires UserName,Password } 

6. API Endoint to Book A Show ---> /api/movies {Body requires JSON Object  {
                                                                          "Select_Seat":"String",
                                                                          "Movie_Name":"String",
                                                                          "Cinema":"String",
                                                                          "City":"String",
                                                                          "Movie_Time":"2020-07-17" 
                                                                          } 
   this Endpoint is only accessible with the autrhorized Admin which will return a bearer token while logging in. 

Database has also been uploaded with MovieDB.rar file
Initial Catalog=MovieDB;User ID=MovieApi;Password=admin@123;
