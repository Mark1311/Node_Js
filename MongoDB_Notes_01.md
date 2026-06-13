# What is MongoDB??
Traditional databases (jaise MySQL ya Oracle) mein data ko tables, rows aur columns mein store kiya jata hai, lekin MongoDB mein aisa nahi hota. MongoDB mein data ko Documents aur Collections ke roop mein store kiya jata hai.

### Key Features
- Schema-less (Flexible): SQL database ki tarah isme pehle se table ka structure (schema) fix nahi karna padta. Agar aapko kisi ek document mein koi extra field (jaise phone_number) add karni hai, toh aap bina baaki data ko chhuye asani se kar sakte hain. 
- Scalability (Sasta aur Tezz): MongoDB Horizontal Scaling ko support karta hai jise Sharding kehte hain. Iska matlab hai ki agar aapka data bohot badh jata hai, toh aap isse asani se multiple servers par distribute kar sakte hain.  
- High Speed: Kyunki isme data ek hi jagah document ke andar mil jata hai (complex JOIN queries ki zaroorat nahi padti), isliye isse data read aur write karna bohot fast hota hai.

# Diff B/w NoSQL and SQL

| Feature / Property | SQL (Relational Database) | NoSQL (Non-Relational Database) |
| :--- | :--- | :--- |
| **Data Storage Format** | Data ko **Tables** (Rows aur Columns) ke roop mein store kiya jata hai. | Data ko **Documents, Key-Value, Columns, ya Graphs** mein store kiya jata hai. |
| **Schema (Structure)** | **Fixed Schema** hota hai. Data insert karne se pehle table structure define karna zaroori hai. | **Dynamic Schema** hota hai. Kisi bhi waqt bina structure badle naya data add kar sakte hain. |
| **Scaling (Vistar)** | **Vertical Scalability** (Server ki RAM, CPU, ya Storage badhani padti hai). | **Horizontal Scalability** (Naye saste servers/nodes add karke capacity badhai jaati hai). |
| **Query Language** | **SQL (Structured Query Language)** ka use hota hai jo standard aur fix hoti hai. | Koi standard language nahi hoti. **Object-based queries** (jaise JSON/BSON) ka use hota hai. |
| **Relationships (Joins)** | Multiple tables ke beech relation hota hai aur **JOIN queries** bohot powerful hoti hain. | Tables nahi hote, isliye **JOINs typically nahi hote**. Data ko ek hi jagah nest kiya jata hai. |
| **Data Types** | **Structured data** ke liye sabse behtar hai (jaise Financial records, User accounts). | **Unstructured ya Semi-structured data** ke liye behtar hai (jaise Logs, Chats, Social Media). |
| **ACID Compliance** | **High ACID compliance** (Atomicity, Consistency, Isolation, Durability) milti hai. Data safe rehta hai. | **BASE properties** follow karta hai. Eventual consistency hoti hai, lekin performance fast hoti hai. |
| **Popular Examples** | MySQL, PostgreSQL, Oracle, MS SQL Server, SQLite. | MongoDB, Redis, Cassandra, DynamoDB, Neo4j. |

# What is BSON?
BSON ka matlab hota hai Binary JSON.Yeh ek aisa data interchange format hai jise main roop se MongoDB mein data ko store karne aur network par transfer karne ke liye use kiya jata hai. Simple bhasha mein, yeh JSON (JavaScript Object Notation) ka ek zyada advanced aur optimized roop hai.
### 1. BSON, JSON se alag kaise hai?
JSON insano ke padhne ke liye bohot asan hai (Human-readable text format), lekin computers ke liye text ko baar-baar read aur parse karna slow hota hai.

BSON isi JSON data ko Binary Format (0s aur 1s) mein convert kar deta hai. Isse computer/database data ko bohot tezi se read, write aur search kar paata hai.

### 2. BSON ke Fayde (Why MongoDB uses BSON?)
Tez Raftar (High Speed): BSON mein har field ke sath uski length aur data type pehle se likha hota hai. Iski wajah se MongoDB ko pura document scan nahi karna padta, woh seedhe skip karke sahi data par pahunch jata hai (इसे Traversal Speed kehte hain).

Zyada Data Types Support: JSON mein sirf basic data types hote hain (jaise String, Number, Boolean, Array, Object, Null). Lekin BSON mein kuch extra aur zaroori data types milte hain:

# Commands:-
> Naya Database banana ya purane me switch karna:
`use my_database`

> Saare databases ki list dekhna:
`show dbs`

> Create Collection
```js
db.users.insertOne({
    name: "Rahul",
    age: 25,
    city: "Delhi"
  })
```
```js
db.users.insertMany([
  { name: "Amit", age: 30, city: "Mumbai" },
  { name: "Neha", age: 22, city: "Pune" }
])
```

> Data ko saaf aur sundar (Formatted)
`db.users.find().pretty()`

> Read Commands (Data Dhundna/Dekhna)
`db.users.find()`
`db.users.find({ city: "Delhi" })`

> Delete Commands (Data Hatana)
`db.users.deleteOne({ name: "Amit" })`

> pura collection (Table) delete
`db.users.drop()`