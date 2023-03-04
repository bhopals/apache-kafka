### Basic Concepts

#### Messages

- KAFKA MESSAGES

  - Kafka Message is a Unit of data that is collected, stored, and distributed by Kafka
  - Event - Kafka Message is also called an EVENT. A message is a real world event at a point in time.
  - Unit of Data - Row, record, Map, Blob
  - Byte Array -Structure imposed by Publisher, Understood by Consumer. And be able to Serialize and Deserialize the message.
  - Size Limit exists in Kafka. It is configurable and the default size is One MB
  - Can be Batched for efficiency - Batch Processing

- KAFKA MESSAGES CONTENT

  - Kafka Message has some predefined attributes (Key, Value, timestamp)
  - Key - Messages in Kafka have a KEY. The Key is defined by the producer of the message. Keys are not mandatory and they also need not to be unique. Keys are used for Partitioning
  - Value - Value contains the actual message. It is a binary/byte array and the semantics of the value is user defined.
  - Timestamps - Every message is automatically timestamped by Kafka. Kafka supports two type of automatic timestamping.

    - Automatially Timestamped
    - Event time v/s Ingestion time
      - Event time is when the message is producer creates a timestamp.
      - Ingestion time is when the kafka broker timestamps it, when it stores record.

  - Kafka Assigns a random key when the KEY is not provided by the producers.

#### Kafka Topics

- Topics in Kafka Hold and Manage Messages
- Topics in Kafka is an ENTITY that holds a message. It is same as Database table (Topic) with records (Messages) of the same type
- Topic can be considered as a Queue for similar messages. Example of Topics - Sales Transations, Audit Logs, Video files
- Kafka supports multiple topics per Kafka instance (Based on the use case)
- Each Topic support multiple Producers to Publish data to the Topic concurrently. Similarly, multiple consumers can consumer data from this topic concurrently.
- Each Topic has multiple Partitions that physically split data across multiple files. Each message will only be stored in one pratition.

KAFKA INSTANCE(1) ==> (N) TOPICS ==> (N) PARTITIONS ==> (N) MESSAGES (KEY, VALUE, TIMESTAMP)

#### Kafka Brokers

- A Kafka Broker is nothing but a RUNNING KAFKA Instance
- It is a Physical Process that runs on the base operating system and executes all Kafka functions.
- A Kafka process Listens on a Specific Port (default-9092 port)
- The Kafka Broker receives message from Producers, and Stores them locally in logs. - Subscription Management - Consumer subscribe to specific topics within the Kafka Broker. The Broker keeps track of all active consumers. It knows about the last message that was sent to Consumer. It also keeps a heartbeat with every consumer, so when a consumer dies, it can track and reset.

- Topics, Partition & Logs Management - Kafka Broker manages the lifecycle of Topics

### KEYWORDS

- Kafka Message - A Unit of data that is Collected, Stored, and Distributed by Kafka
- Semantics of the Value
- Topics in Kafka Hold and Manage Messages
- Kafka Broker is a Physical Process that runs on a Base Operating System and executes all Kafka functions.
- Kafka Process/Broker listens on a specific Port.
