<h1 align="center"><u>PysonDB</u></h1>

* [Install](https://github.com/fredysomy/pysonDB) 
* [Example Code](https://github.com/fredysomy/pysonDB/tree/master/example) 
* [Command Line Operations](https://fredysomy.me/pysonDB/docs/cli) 
* [Adding Data](https://fredysomy.me/pysonDB/docs/add) 
* [Get data](https://fredysomy.me/pysonDB/docs/get) 
* [Search data](https://fredysomy.me/pysonDB/docs/re_search) 
* [Update Data](https://fredysomy.me/pysonDB/docs/update) 
* [Delete Data](https://fredysomy.me/pysonDB/docs/delete)

<h2>Get Data</h2>

* There are three methods to get data.
  * get(n, objectify=False)
  * getAll(objectify=False)
  * getBy(query, objectify=False)
  * find(id)


<h2><code>get()</code></h2>

* returns only one data by default.

* get(3) => retruns 3 json data. 

path.json

```json
{"data":[{"name":"pysondb","type":"DB"},{"name":"py_cli","type":"CLI"},{"name":"py_cli2","type":"CLI"}]}
```

```python
>> from pysondb import db
>> a=db.getDb("path.json")
>> a.get()
>> [{"name":"pysondb","type":"DB"}]
>> a.get(1)
>> [{"name":"pysondb","type":"DB"},{"name":"py_cli","type":"CLI"}]

```
<h2><code>getAll()</code></h2>

* Returns all data in the database

```python
>> from pysondb import db
>> a=db.getDb("path.json")
>> a.getAll()
>> [{"name":"pysondb","type":"DB"},{"name":"py_cli","type":"CLI"},{"name":"py_cli2","type":"CLI"}]

```
<h2><code>getBy(query)</code></h2>

* getBy(query)  query must be a JSON data.
* getBy({"type":"CLI"})

```python
>> from pysondb import db
>> a=db.getDb("path.json")
>> a.getBy({"type":"CLI"})
>> [{"name":"py_cli","type":"CLI"},{"name":"py_cli2","type":"CLI"}]
>> a.getBy({"name":"py_cli"})
>> [{"name":"py_cli","type":"CLI"}]
```

<h2><code>find(id)</code></h2>

* find(id) : Id must be a Int.
* find(23234234345345345)

```python
>> from pysondb import db
>> a=db.getDb("path.json")
>> a.getAll()
>> [{"name":"pysondb","type":"DB",id:1234},{"name":"py_cli","type":"CLI",id:5678},{"name":"py_cli2","type":"CLI",id:9101112}]
>> a.find(1234)
>> {"name":"pysondb","type":"DB",id:1234}
```


* See full examples [here](https://github.com/fredysomy/pysonDB/example). 
* If You have any queries or doubts join the discord server [here](https://discord.gg/SZyk2dCgwg)