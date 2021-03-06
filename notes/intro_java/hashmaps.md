HashMaps
========

The [Java Collections framework](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/overview.html) provides several data structures that are useful for various types of programs.

The `HashMap` is very similar to a dictionary in python. It maps keys to values and if you have the desired key you can retrieve the associated value with one operation. A search (linear or binary) is not necessary.

The following creates a `HashMap` that will map `String` objects to `String` objects. This could be used to store a mapping from names to office locations, for example "Sami Rollins" -> "HR 544".

```java
HashMap<String, String> officeLocations = new HashMap<String, String>();
```

The next example creates a `HashMap` that will map `Integer` objects to `Name` objects. This could be used to map a numerical ID number to a `Name` object containing the first and last name of the person with the ID.

```java
HashMap<Integer, Name> result = new HashMap<Integer, Name>();
```

To insert data into a `HashMap` you use the `put` operation as follows:

```java
officeLocations.put("Sami Rollins", "HR 544");
officeLocations.put("Rosa Maria Garay", "HR 545");
```

To retrieve data from a `HashMap` you use the `get` operation as follows:

```java
System.out.println(officeLocations.get("Sami Rollins")); //print HR 544
```

You can iterate over all of the keys in a `HashMap` and retrieve their associated values:

```java
for(String key: officeLocations.keySet()) {
	System.out.println(key + " " + officeLocations.get(key));
}
```

You can also iterate over all of the values in a `HashMap`, but cannot get the key associated with a specific value without iterating over the entire map:

```java
for(String value: officeLocations.values()) {
	System.out.println(value);
}
```