 Lets first see what a HashMap is:

HashMap is an implementation of Map interface which stores key/value pairs.
main benefit: adds/retrieves elements by key in a constant time
The below code creates a HashMap

```
HashMap<String, Integer> map = new HashMap<>();
```

Here a hash map is created. Consider hash map is a array and one element of that array is known as a bucket. By default say that hash map is created it contains 16 buckets (indexed from 0 to 15)

Now lets insert a key value pair to our map
```
map.put("apple",25);
```

At this point the following things happen internally
- **Calculate the hash code of the key "apple"**
  Hash code calculated using hashCode() method. By default returns the memory reference of object in integer form. The process of converting an object into integer by using the method hashCode() is called hashing. We can override the hashCode() method to define our own implementation.

- **Calculate the index**
  Since hash code generated for a key is a large number, we need to generate an index which is not greater than the size of our array (which is 16)
  ```
  index = hashCode(key) & (n-1)
  ```
  where n = number of buckets 

- **Create a node object**
  Since we have a key value pair we create a node to store them. Node can have hashcode, key, value and next (which contains address of the next node)

- **Place the created node**
  Now place the create in one of the buckets. Say if we got the index as 5 then place the node in the bucket-5

Let insert another key value pair
```
map.put("banana",30);
```

At this point the following things happen internally
- **Calculate the hash code of the key "banana"**

- **Calculate the index**

- **Create a node object**

- **Place the created node**
  Say if we got the index as 7 then place the node in the bucket-7

Let insert another key value pair
```
map.put("mango",40);
```
At this point the following things happen internally
- **Calculate the hash code of the key "mango"**

- **Calculate the index**

- **Create a node object**

- **Place the created node**
  Say if we got the index as 5. But in bucket-5 we already have a node. Hence there is a collision. What we do is we link the node(apple) with the newly created node(mango), i.e. we place the address of mango node in the next portion of apple node.

![image](https://user-images.githubusercontent.com/39855032/160325999-d1687fe4-3509-41d8-9b9b-032ae5a13980.png)
