# Tutorial-Kafka-Go
## Task:

- Write a consumer in Golang which consumes events from a topic called location indefinitely.

- Write a producer in Golang which produces events every 10 seconds to the location topic indefinitely.

- The event structure that is to be fired and consumed is to be of the following:

Event Key: Customer ID (int64) // You can generate a random integer as the key.<br>

Event Body:<br>
{<br>
       "latitude": (float64), // A random float64<br>
       "longitude": (float64) // A random float64<br>
}<br>

- Both the producer and consumer must be written using the Sarama library (https://github.com/Shopify/sarama).

- Both the producer and consumer must connect to a locally running instance of Kafka.

- Before the producer publishes the event, the event body must be serialized to avro using the goavro library (https://github.com/linkedin/goavro) and when the consumer consumes the event, the body must deserialize the body back to a struct and log the event to the terminal (deserialize should also done by the same goavro library).

- The producer must log the entire event in the terminal before publishing each event. And the consumer must log each event in the terminal after consuming each event.

- All of this code must be pushed to a Github repository with clear explanations on how to build and run the binary.



Links:

[goavro library](github.com/linkedin/goavro)

[Writing and Testing an Event Sourcing Microservice with Kafka and Go](https://semaphoreci.com/community/tutorials/writing-and-testing-an-event-sourcing-microservice-with-kafka-and-go)
