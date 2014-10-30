## DAO ##

### Overview ###

### General Design Considerations ###
- **Choose an appropriate data access technology.**(REST, WebSQL, FileSystem, ...)
- **Use abstraction to implement a loosely coupled interface to the data access layer.**
This can be accomplished by defining interface components, such as a gateway with well-known inputs and outputs, which translate requests into a format understood by components within the layer. In addition, you can use interface types or abstract base classes to define a shared abstraction that must be implemented by interface components.
- **Encapsulate data access functionality within the data access layer.**
The data access layer should hide the details of data source access. It should be responsible for managing connections, generating queries, and mapping application entities to data source structures. Consumers of the data access layer interact through abstract interfaces using application entities such as custom objects and should have no knowledge of the internal details of the data access layer.
- **Decide how to map application entities to data source structures.**
- **Decide how you will manage connections.**
As a rule, the data access layer should create and manage all connections to all data sources required by the application.
- **Determine how you will handle data exceptions.**
- **Consider security risks.**
- **Reduce round trips.**
- **Consider performance and scalability objectives.**

### Specific Design Issues ###
- **Batching**
- **Connections**
- **Data Format**
- **Exception Management**
- **Object Relational Mapping**
- **Queries**

### Connections ###
Connections to data sources are a fundamental part of the data layer. All data source connections should be managed by the data layer. Creating and managing connections uses valuable resources in both the data layer and the data source.


### Relevant Design Patterns ###
- General (Active Record, Data Mapper, Data Transfer Object, Domain Model, Query Object, Repository, Row Data Gateway, Table Data Gateway)
