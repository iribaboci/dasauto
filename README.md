# Description 
This is challenge task with Scala programming language in Play Framework. The task is to develop an REST API for car advertisement. 
 - It is developed in Play Framework with Scala programming language.
 - Used Slick with Mysql database. 
 - Data is represented in Json format.

# Setup

 - Import the SQL file (AutoScout24Demo.sql) to mysql database.
 - Open project and build it.
 - Execute 
```bash
sbt run
```

# REST API 

1 - <b>List all car adverts :</b> 
  - The car adverts are listed and by default are sorted by id.
```bash
curl -i -X GET http://localhost:9000/
```

  - You can choose by which filed you want to sort the listed car adverts.
```bash
curl -i -X GET http://localhost:9000/listcars/"name of the field"
```

2 - <b>Get car advert by ID :</b>
  - You can show an car advert by using the ID of the car advert
  ```bash
curl -i -X GET http://localhost:9000/getcar/"the ID number of car advert"
```

3- <b>Add car advert :</b>
POST json object to add new car advert
  ```bash
{
	"title": "Fiat",
	"fuelId": 1,
	"price" : 233224323,
	"newCar": true
}
```

4- <b>Modify car advert :</b>
POST the json object with id to modify the car advert
  ```bash
{
	"id": 22,
	"title": "Fiat_modified",
	"fuelId": 1,
	"price" : 233224323,
	"newCar": true
}
```

5- <b>Delete car advert :</b>
  ```bash
curl -i -X POST http://localhost:9000/car/deleteCar/"the ID number of car advert"
```


# Improvements
 - Create a build in database like H2 or Learn about aws DynamoDB and replace MySql to aws DynamoDB 
 - Create Controller tests
 - CORS Request support
