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