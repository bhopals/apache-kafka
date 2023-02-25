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

  - Kafka Assigns a random key when the KEY is not provided.

### KEYWORDS

- Kafka Message - A Unit of data that is Collected, Stored, and Distributed by Kafka
- Semantics of the Value
