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

### Keywords

- Building Distriuted Services
- Multiple Running Process Instances
- Strong Static Binding
- Multiple Senders and Receivers exchanging the same type of data between them
- Publish Subscribe Pattern
- Clean and Scalable Solution
- Decoupling of Publisher and Subscriber
- Back-Pressure Handling
