## What is redis?
- redis stands for remote dictionary server
- written in C by Sanfilippo in 2006
- a NoSQL advanced key-value store 
- stores all data in memory so read and write is very fast

redis is often referred to as a data structure server 

## Redis data types

Redis is a key-value store
The key in Redis is a binary-safe String

Binary-safe string is a string that can contain any kind of data or a serialized Java object

## String
String is the simplest type of value that can be associated with a key in Redis

Memcached is an open-source distributed memory caching system
Memcached stores data in key-value pairs

## List 
List type is useful for storing a collection of strings in Redis
The elements are stored in a linked list 
- quick insertion and removal of the element from the head
- sorted on the basis of insertion order
- list should be stored in those cases where the order of insertion matters
  - storing logs

## Set
- Doesn't allow duplicates | elements are not sorted in any order
- constant time performance for adding and removing operations 

Lexicographic order is dictionary order, except that all the uppercase letters comes before the lowercase letters

## Hash
Hash value type is a field-value pair

## Insertion and Retrieval Commands
- Simplest form of data that can be stored in the Redis database is String
  - we can store static html pages in the Redis database where the key is some name used to identify the page and value is the HTML String

### SET -- Store a record in redis 
SET key value 
SET apple 300

### GET -- get the value of a key
GET key

### SETX -- set a certain time after which the key will be removed from the db 
SETEX key seconds value

### PSETEX -- the time is in milliseconds
PSETEX key millisecond value


### SETNX -- Set if not exists
SETNX key value
- sets a key to a value only if the key does not already exist 


### STRLEN: find the length of the value for a particular key
STRLEN key 


### MSET: save multiple records in a single command
MSET key1 value1 key2 value2


### MGET: get the value of multiple keys in a single command
MGET key1 key2


