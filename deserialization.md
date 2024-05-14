# Deserialization 

## Python

Unsafe code:

```python
pickle.loads()
yaml.load()
jsonpickle.encode()
jsonpickle.store()
```
## Java

Unsafe code:

```java
XMLDecoder
XStream fromXML()
ObjectInputStream readObject()
ObjectInputStream readResolve()
ObjectInputStream readExternal()
ObjectInputStream readUnshared()
Serializable
```

Safe code:

```java 
private final void readObject(ObjectInputStream in) throws java.io.IOException { //readObject() must be final and always throw an exception
    throw new java.io.IOException("Cannot be deserialized");
}

fastJson
json-io
kyro
Yamlbeans
```
