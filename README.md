# Dependency Injection

There are tree lifetime

1. Singleton - Singleton lifetime servers are created the first time they are created.
2. Scoped - Scoped lifetime services are created once per request.
3. Transient - Transient lifetime services are created each time they're requested.

> **Notes about scoped lifetime**  
*In The Middleware*, Don't inject the services in to the constructor that their lifetime is scoped.

> **Note about singleton lifetime**  
Don't resolve a scoped service from a singleton. It may cause the service have incorrect state when processing subsequent requests.

## Design services for dependency injection

- Design Services to use dependency injection to obtain their dependencies.
- Avoid stateful, static method calls

