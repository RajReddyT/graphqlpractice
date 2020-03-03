# graphqlpractice
This is a practice session for graphql.

1. What is graphql ? <br>
a. The problem that is present in REST — Under or Overfetching of data <br>
    Overfetching— takes place when more data is fetched than required.
    Underfetching — opposite, takes place when not enough data is delivered upon fetching. 
    It solved by GraphQL — you get exactly data that you requests.
2. Relational exploration : GraphQL can specify relations among the entities and their required fields, on the other hand, graphql engine
sorts the relations and wanted fields automatically and returns the results to the client application.

Prerequisites
1. Please install JDK 8 +
2. Install Mongo database ( community/licensed) as per convenience 
3. Java IDE 

Following are the Application Setup instructions
1. Check out https://github.com/RajReddyT/graphqlpractice.git
2. Execute mvn clean build
3. Run mvn spring-boot:run
that's it, it boots the application

Following are the data setup instructions

1. Create database with the name "graphql" 
2. Create collections with the names "users" and "articles" 

Pleaes insert into "users" collection
<pre>
{
    "_id" : "User1",
    "name" : "Ram",
    "age" : 38,
    "nationality" : "Indian",
    "createdAt" : "2020-03-01"
}

/* 2 */
{
    "_id" : "User2",
    "name" : "Shyam",
    "age" : 35,
    "nationality" : "Indian",
    "createdAt" : "2020-03-01"
}

/* 3 */
{
    "_id" : "User3",
    "name" : "Suresh",
    "age" : 34,
    "nationality" : "Indian",
    "createdAt" : "2020-03-01"
}

/* 4 */
{
    "_id" : "User4",
    "name" : "Naresh",
    "age" : 36,
    "nationality" : "Indian",
    "createdAt" : "2020-03-01"
}

/* 5 */
{
    "_id" : "User5",
    "name" : "Mahesh",
    "age" : 38,
    "nationality" : "Indian",
    "createdAt" : "2020-03-01"
}
</pre>

<B> 
Please insert following into "articles" collection
</B>

<pre>

{
    "_id" : ObjectId("5e5b76550d7ed366101ff3cb"),
    "title" : "Head First Java",
    "minutesRead" : 60,
    "authorId" : "User1"
}

{
    "_id" : ObjectId("5e5b767a0d7ed366101ff3dd"),
    "title" : "Mongo mechanics",
    "minutesRead" : 60,
    "authorId" : "User1"
}


{
    "_id" : ObjectId("5e5b769e0d7ed366101ff3ea"),
    "title" : "NodeJs ",
    "minutesRead" : 60,
    "authorId" : "User2"
}

{
    "_id" : ObjectId("5e5b76cf0d7ed366101ff3fb"),
    "title" : "MongoDB or Dynomo DB",
    "minutesRead" : 30,
    "authorId" : "User3"
}

/* 5 */
{
    "_id" : ObjectId("5e5b76db0d7ed366101ff404"),
    "title" : "Head First Java",
    "minutesRead" : 60,
    "authorId" : "User5"
}
</Pre>

Once application is up and runnig.

1. Use any rest client with POST method and use the following url http://localhost:8000/query   
2. Query 
     Query to fetch all the fields 
     <pre>
     
     {
      users {
        name
        articles {
          title
        }
      }
    }
   </pre>
   
  Fetch specified user
  
  
