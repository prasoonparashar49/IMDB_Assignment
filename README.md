
# IMDB_WebApp
This is made using MVC and Entity Framework.
It is using Code First Approach to create the database, hence there is no need of any DB Script

Class __IMDBInitializer.cs__ initializes Database with some seed values. 

In __Web.Config__, change connection string to the database that you want
  ```
    <connectionStrings>
    <add name="DefaultConnection" connectionString="Data Source=(localdb)\v11.0;AttachDbFilename=|DataDirectory|\aspnet-IMDB_WebApp-20180604073403.mdf;Initial Catalog=aspnet-IMDB_WebApp-20180604073403;Integrated Security=True" providerName="System.Data.SqlClient" />
  </connectionStrings>
  ```
  
  ***(localdb)\v11.0*** above  is the database instance I am connected to. Just change it to the connection instance you want to connect to

The app _Drop And Create database_ everytime you exectue it. So, make sure that you closes the connection to the database before executing the app. Otherwise, it may throw exception when you run app or try to create movie.

First create movie before browsing or editing it. Link for creating movie is _/Movie/CreateMovie_



## INSTRUCTIONS TO EXECUTE THE APP

1. zip the file from the github

2. Download the zip file

3.__IMDB_Assignment__ is the parent folder. __IMDB_WebApp__ contains the web app. __.sln__ file is in parent folder. Open __.sln__ file using Visual studio. It should work


## URL
1.url for creating movie  __/Movie/CreateMovie__

2.url for listing movies  __/Movie/Index__

3.url for editing movie   __/Movie/EditMovie/id__

4.url for creating actor  __/Actors/Create__

5.url for creating producer  __/Producers/Create__

## Important Points
1.In Movie Creation page and Edit page, Ensure that you are selecting actors. I have not covered the case where user is not selecting any actor. It may lead to exception

2.Make sure that you are not uploading large image. There are some images in the Image folder that you can use to test. copy few images to some location and delete the remaining images.

3.I am using DateTime as the data type for the Date input type. A valid literal for date is _1/1/0001 12:00:00 AM_ 