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
* Find bands an sort by label 
* Find all bands on tour
* Find bands of specific genre

### People
Import people.json as described above.

* Find all people of an exact age
* Find all people over 35
* Find all people under 35
* Find all active people
* Find all people who do not have strawberries as their favorite fruit
* Find all people and sort them by age