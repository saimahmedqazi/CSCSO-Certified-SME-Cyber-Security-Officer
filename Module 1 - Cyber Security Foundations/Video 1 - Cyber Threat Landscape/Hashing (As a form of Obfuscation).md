### Definition

**Hashing** is a one-way cryptographic process that turns an input (like a password) into a fixed-length string of characters (a "hash") that cannot be reversed.

### Explanation

In the context of **Data Obfuscation**, hashing is used because it "hides" the original data permanently. Unlike encryption, there is no "key" to turn a hash back into a password. To verify a user, the system simply hashes the _new_ attempt and sees if it matches the _stored_ hash.

- **Scenario:** 🔐 An employee creates the password `ChocolateCake123`. The system immediately hashes it to something like `a1b2c3d4...`. Even if a hacker steals the database, they only see the "scrambled" code. They can't tell the employee likes chocolate cake; they just see a meaningless string of data.
    

### Example
#
- **SHA-256:** A common modern algorithm that produces a 64-character hash.
    
- **Salting:** Adding random data to a password _before_ hashing it to ensure that even if two users have the same password, their obfuscated hashes look different.