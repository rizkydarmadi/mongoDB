# mongo note

## Mongo Shell

- Via docker

```bash
sudo docker -exec -it {your docker container name eg: mongo} bin/sh
```

- connect mongo shell

```bash
mongo --host localhost --port 27017
```

## create database

```js
use your_database_name
```

## show current database

```js
db;
```

## show all databases

```js
show databases
```

## show all collections

```js
show collections
```

## create collection

```js
db.createCollection("your name collection");
```

## insert

```js
db.customers.insertOne({
  _id: "tays",
  name: "taylor swift",
});
// insert many
db.customers.insertMany([
  {
    _id: "adam",
    name: "adam levine",
  },
  {
    _id: "eddie",
    name: "ed sheeran",
  },
]);
```

## select all in collection

```js
db.your_collection.find();
```

## update One and Many

```js
db.your_collection.updateOne(
  { _id: 181011402252 },
  { $set: { name: "bernadya" } }
);
db.your_collection.updateMany({ size: "xl" }, { $set: { size: "l" } });
```

## delete One and Many

```js
db.your_collection.deleteOne({ _id: 1 });
db.your_collection.deleteMany({ name: "socks" });
```
