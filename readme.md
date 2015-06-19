# Mongo Find Practice

## Setup
Make sure `mongod` is running in another tab.

```
mongoimport --jsonArray --db practice --collection bands --file bands.json

```

```
use practice
db.bands.find()
```

### Bands
Import bands.json as described above.

* Find all bands

`db.bands.find()`

* Find bands an sort by label 

`db.bands.find().sort({label: 1})`

* Find all bands on tour

`db.bands.find({onTour: true})`

### People
Import people.json as described above.

* Find all people of an exact age

`db.peopletest.find({age: 36})`

* Find all people over 35

`db.peopletest.find({age: { $gt: 35}}, {name: 1})`

* Find all people under 35

`db.peopletest.find({age: { $lt: 35}}, {name: 1})`

* Find all active people

`db.peopletest.find({isActive: true}, {name: 1})`

* Find all people and sort them by age

`db.peopletest.find({}).sort({age: 1})`

* Find all people who do not have strawberries as their favorite fruit

`db.peopletest.find({age: { $ne: 'strawberry'}})`
