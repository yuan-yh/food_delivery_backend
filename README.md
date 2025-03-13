# sky-take-out

Maven Parent Project:

- Unified Dependency Version Management: define the versions of dependencies shared by all submodules in pom.xml, avoiding version conflicts or inconsistencies when each submodule defines dependencies separately.

- Aggregation of Submodules: The parent project aggregates multiple submodules (e.g., sky-common, sky-pojo, sky-server) for unified build and management.


## sky-common

Submodule - a common module that stores shared code and utility classes used across the project to avoid code duplication and improve reusability.

Content:

- Utility Classes (Utils): Commonly used utility methods, such as date processing, string manipulation, encryption, etc.

- Constant Classes (Constants): Defines constants used in the project, such as status codes or configuration items.

- Exception Classes (Exceptions): Custom exception classes for handling business logic exceptions uniformly.

## sky-pojo

Submodule - store data models and related classes, centralizing the management of data models for easier maintenance and scalability.

Content:

- Entity Classes: Java classes corresponding to database tables, typically mapped using ORM frameworks like JPA or MyBatis.

- VO (View Object): Data objects used for frontend display, often encapsulating or simplifying entity classes.

- DTO (Data Transfer Object): Objects used for transferring data between different layers, such as between the Controller and Service layers.

## sky-server

Submodule - the core module of the backend service, responsible for handling business logic, data interaction, and exposing APIs.

Content:

- Configuration Files: Stores project configuration files, such as application.yml or application.properties, for configuring database connections, logging, caching, etc.

- Controller: Handles HTTP requests, receives parameters from the frontend, invokes the Service layer for business logic processing, and returns results to the frontend.

- Service: Implements core business logic, such as data processing and business rule validation.

- Mapper: Interfaces or implementations for interacting with the database, typically using ORM frameworks like MyBatis or JPA.
