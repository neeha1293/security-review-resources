# Insecure Random Generators:

##Java

Unsafe:
```java
java.util.Random
```

Safe
```java
SecureRandom
```

## Python

Unsafe:
```python
random.random()
random.randInt(0,100);
static IV = '12345'; //using static IV for encryption in AES

```

Safe:
```python
secrets.choice(seq)
secrets.randbelow(bound)
secrets.randbits(k)
secrets.token_bytes(32)
secrets.token_hex(16)
secrets.token_urlsafe(16)
secrets.compare_digest(a,b)
```

##Node.js

Safe:
```node.js
crypto.randomBytes()
