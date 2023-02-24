### Introduction to Kafka

#### Messages Queues

- When we build distributed services, we have multiple running process instances that communicate with each other over the network to exchange messages.

- Let us start with the simple two process network where a sender process communicates with the receiver process to exchange data. In this case, the sender need to know the address of the receiver process. In addition both the sender and the receiver needs to agree upon a common data protocol and far more. This creates a STRONG STATIC BINDING between the two processes.
  If we have more receivers than the sender needs to be aware about all the receivers. But what happens when you have MULTIPLE SENDERS and MULTIPLE RECEIVERS exchanging the same type of data between them.

- The above scenario gets more complex with multiple receivers and senders. And if we add Fault tolerance to it, things will get more complicated/complex.

- The Clean and Scalable solution here is to use a MESSAGE QUEUE. Each sender needs to only know about the message queue, and simply publish the messages to the Queue. A receiver becomes a subscriber and subscribe to the message queue. When a new message available in the queue, the subscriber is notified who then proceeds to pull the message and use it. The both subscribers and publishers are unaware about each other, and only need to know about the Message QUEUE. This is Publish Subscriber Patterns also called PUB-SUB.

- PUB-SUB Advantages
  - Decoupling of Publishers and Subscribers
  - Easy Management and Changes
  - Scaling (N+1)
  - Back-pressure Handling - Cache Data till Subscriber consumes it
  - Reliability through persisting Queue data and tracking consumption of data

#### What is Kafka

- What is Apache Kafka?

  - Kafka is Events/Messages Streaming Platform
  - Events and Messages represents the actual data that is exchanges through Kafka
  - Critical piece of the Big Data puzzle
  - Open-source with Commercial options
  - Most popular messaging plaform in the world
  - Producers (Publishers) push messages to Kafka
  - Consumers (Subscribers) listen and receive messages from Kafka
  - Producers and Consumers are standard terms to represent Publishers and Subscribers

- What Capabilities does Kafka Provide for data exchange? (Kafka Data Functions)
  - Collection - It collects messages from Multiple producers concurrently
  - Storage - It provides persistent storage of the messages received
  - Fault Tolerance Capabilities
  - Transport - It transports data across from Producers to Consumers. With mirroring capabilities, it can also transport data across networks
  - Distribution - It distributes data to multiple concurrent consumers for downstream processing
  - Tracking - It provides tracking of message consumption by each consumer. This ensures atleast once delivery of messages even if the consumers go down and come back again

### Keywords

- Building Distriuted Services
- Multiple Running Process Instances
- Strong Static Binding
- Multiple Senders and Receivers exchanging the same type of data between them
- Publish Subscribe Pattern
- Clean and Scalable Solution
- Decoupling of Publisher and Subscriber
- Back-Pressure Handling

- Kafka is Events/Messages Sreaming Platform
- Producers and Consumers
- Exchange message through Kafka
- Producers and Consumers
- Persistant Storage
- Fault Tolerance Capabilities
- Exchange messages and events
- Transports data across from Producers to Consumers
- With Mirroring Capabilities, it can transport data across the networks
- Distribute data to multiple concurrent consumers for downstream processing
- Downstream processing
- Message consumption
- Ensure once delivery of the messages
