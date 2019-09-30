## Quiz: ORM

???

# ORM

?: Object Relational Mapping (ORM) is the technique of accessing a relational database using what type of programming language?

( ) SQL ( ) Ruby ( ) BASH (X) Object-Oriented

?: What Ruby method can be used to insert data into the database?

( ) `.insert` ( ) `.add` (X) `.save` ( ) `.update`

?: To follow a pattern of _logical design_, if we have a `Car` class, what should the table be named?

(X) `car` ( ) `make` ( ) `model` ( ) `vehicle`

?:

```ruby
class Car

  attr_accessor :make, :model

  def initialize(make, model)
    @make = make
    @model = model
  end

end
```

In order to "map" this `Car` class to a `cars` database table, what needs to be done first?

( ) Create a `cars` table (X) Create a database ( ) Make a `.create_table` method ( ) Add an `id` argument to the `#initialize` method that defaults to `nil`.

?: Which method would update the database row mapped to the given instance?

( )`.save` (X)`.update` ( )`.find` ( )`self`

?: To set a constant named `DB` that contains a connection to a database, which syntax should be used?

( )
```ruby
DB = {conn => SQLite3::Database.new("db/database.db")}
```
( )
```ruby
DB = {:conn => SQLite3::Database("db/database.db")}
```
( )
```ruby
db = {:conn => SQLite3::Database.new("db/database.db")}
```
(X)
```ruby
DB = {:conn => SQLite3::Database.new("db/database.db")}
```

?: To map a class to a database table, create a table with the same name as the class and give use table column names that match the `attr_accessors` of the class.

(X) True ( ) False

?:

| id | make | model |

Which code snippet maps the instance attributes to these table columns?

( )
```ruby
class Car

  attr_accessor :make, :model, :id

  def initialize(make, model, id)
    @id = id
    @make = make
    @model = model
  end

end
```
( )
```ruby
class Car

  def initialize(make, model, id=nil)
    @id = id
    @make = make
    @model = model
  end

end
```
(X)
```ruby
class Car

  attr_accessor :make, :model, :id

  def initialize(make, model, id=nil)
    @id = id
    @make = make
    @model = model
  end

end
```
( )
```ruby
class Car

  def initialize(make, model, id=nil)
    @id = id
    @make = make
    @model = model
  end

end
```

?: It is best to save a new record when a new object is created, i.e. in the `#initialize` method.

( ) True (X) False


???
