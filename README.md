<p align="center">
  <a href="https://fastapi.tiangolo.com"><img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI"></a>
</p>

# FastAPI

FastAPI is a modern, high-performance Python web framework used to build APIs.

### What is API ?
- API stands for Application Programming Interface.
- API is a set of rules and protocols that allows different software applications to communicate with each other.
- It acts as a software intermediary which enables one program to request data or actions from another program without needing to understand the underlying internal code or implementation details



### HOW REQUEST MOVE ?

```txt
Frontend → FastAPI → Database / External API
    ↑                       ↓
    └────── JSON Response ──┘
```    

### Learn More

```txt
┌─────────────────┐
│    FRONTEND     │
│ HTML/CSS/JS     │
│ React, Vue, etc.│
└────────┬────────┘
         │
         │ HTTP Request
         │ (GET, POST, PUT, DELETE)
         ▼
┌─────────────────┐
│     FASTAPI     │
│    BACKEND      │
│                 │
│  API Endpoints  │
│  Business Logic│
└────────┬────────┘
         │
         │
    ┌────┴─────────────┐
    ▼                  ▼
┌───────────┐   ┌──────────────┐
│ DATABASE  │   │ EXTERNAL API │
│ PostgreSQL│   │ Weather API  │
│ MySQL     │   │ Payment API  │
└───────────┘   └──────────────┘
         │                  │
         └────────┬─────────┘
                  │
                  ▼
           Processed Data
                  │
                  ▼
           JSON Response
                  │
                  ▼
┌────────────────────────────┐
│          BROWSER           │
│ Displays the received data │
└────────────────────────────┘
```

### Is the FastAPI is the Only API Framework ?

- There are many API Web Frameworks
Example : Programming Language → API Framework
```txt
Python → FastAPI, Django, Flask
JavaScript → Express, NestJS
Java → Spring Boot
Go → Gin, Fiber
```

- The browser doesn't care what language the backend uses.


## Why Was FastAPI Created?

### Before FastAPI, Python developers commonly used frameworks such as:

- Flask
- Django
- Django REST Framework

### Although these frameworks are powerful, developers often needed additional tools or configurations for:

- Input validation
- API documentation
- Type-based request handling
- Asynchronous programming

## How FastAPI Works
Request Flow

```txt
        Client
          │
          ▼
   HTTP Request
          │
          ▼
      FastAPI
          │
          ▼
   Input Validation
          │
          ▼
    Business Logic
          │
          ▼
    ML Model / DB
          │
          ▼
   Prediction Result
          │
          ▼
    JSON Response
```    

- FastAPI acts as the communication layer between the client and the backend logic.


## Key Features of FastAPI

| Feature                 | Description                                                               |
| ----------------------- | ------------------------------------------------------------------------- |
| High performance        | Built on ASGI technologies and suitable for high-concurrency applications |
| Automatic documentation | Generates interactive Swagger UI and ReDoc documentation                  |
| Data validation         | Validates request data using Pydantic                                     |
| Type hints              | Uses Python type hints to improve development and validation              |
| Asynchronous support    | Supports `async` and `await`                                              |
| Easy API development    | Reduces boilerplate code                                                  |
| Dependency injection    | Provides a system for managing dependencies                               |
| OpenAPI support         | Automatically generates an OpenAPI specification                          |


## FastAPI vs Flask vs Django

| Feature                     | FastAPI                        | Flask                                                         | Django                                            |
| --------------------------- | ------------------------------ | ------------------------------------------------------------- | ------------------------------------------------- |
| Primary use                 | APIs and backend services      | Web applications and APIs                                     | Full-stack web applications                       |
| Performance model           | ASGI-friendly                  | Traditionally WSGI, with modern async support                 | Full-stack framework with async capabilities      |
| Automatic API documentation | Built-in                       | Requires extensions                                           | Requires additional tools                         |
| Data validation             | Pydantic integration           | Usually requires additional libraries                         | Forms and serializers through relevant components |
| Learning curve              | Moderate                       | Relatively easy                                               | Higher                                            |
| Built-in ORM                | No                             | No                                                            | Yes                                               |
| Async support               | Excellent support              | Available, with limitations depending on deployment and usage | Available                                         |
| Best suited for             | API services and microservices | Lightweight applications                                      | Large, feature-rich web applications              |



## Limitations of FastAPI

- It does not include a built-in ORM.
- Developers must select and configure database tools.
- Understanding asynchronous programming can take time.
- It does not automatically make CPU-intensive ML computations faster.
- Authentication, authorization, and deployment still require proper implementation.

- FastAPI is a framework, not an entire backend architecture.

## Applications of FastAPI

- REST APIs
- Microservices
- Machine-learning model serving
- AI application backends
- Data-processing services
- Authentication services
- Real-time backend systems
- Cloud-based applications

## Behind FastAPI Framework 

FastAPI is built on top of two primary Python libraries: ``Starlette`` and ``Pydantic``.

### Starlette

- Starlette handles the web framework aspects
- including the asynchronous ASGI (Asynchronous Server Gateway Interface)
- protocols, routing, middleware, and server capabilities.

### Pydantic

- Pydantic is responsible for data validation,
-  serialization, and deserialization using standard Python type hints.




## Research 

### fast api is built on top of pydantic then why do we need to import pydantic explicitly ?

- FastAPI is built on top of Pydantic, but it does not automatically import or expose Pydantic classes (like BaseModel) in your code namespace

- We must explicitly import ``BaseModel`` from ``pydantic`` because ``FastAPI`` relies on ``standard Python type hints`` to define your data structures, 
- rather than using its own proprietary model syntax. 


## Official Read/Research Sources
- FastAPI Documentation: https://fastapi.tiangolo.com/
- FastAPI GitHub Repository: https://github.com/fastapi/fastapi
- Pydantic Documentation: https://docs.pydantic.dev/
- Starlette Documentation: https://www.starlette.io/