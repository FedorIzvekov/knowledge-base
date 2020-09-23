[Return to main README.md](../README.md#knowledge-base)

# Database

## ACID on Transaction Flow

<img src="./files/acid.png" alt="ACID on Transaction Flow" height="800"/>

## SQL Isolation Levels

| Isolation Level      | Guarantee                   | Allowed Anomalies                                           | ACID: Isolation |
| -------------------- | --------------------------- |-------------------------------------------------------------|-----------------|
| **Read Uncommitted** | Sees uncommitted changes    | Dirty read <br>Non-repeatable read <br>Phantom read         | ❌ None          |
| **Read Committed**   | Only sees committed data    | Non-repeatable read <br>Phantom read                        | ⚠️ Weak         |
| **Repeatable Read**  | Repeatable reads guaranteed | Phantom read <br>(in PostgreSQL or CockroachDB NOT allowed) | ✅ Strong        |
| **Serializable**     | Full transaction isolation  | No anomalies                                                | ✅ Full          |

* Dirty read — reading uncommitted data
* Non-repeatable read — same query yields different results
* Phantom read — new rows appear on re-execution of a query