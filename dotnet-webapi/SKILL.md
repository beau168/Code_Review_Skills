---
name: DotNet-WebAPI-Review
description: Guidelines for reviewing C# .NET Framework Web API projects.
---

# .NET Framework (Web API) Code Review Guidelines

## 🏗️ Architecture & SOLID
- **SOLID Principles**: Ensure classes are small, focused, and follow SOLID principles.
- **Dependency Injection**: Use DI containers where possible. Avoid `newing` up dependencies in constructors.
- **Repository Pattern**: Check for proper abstraction between data access and business logic.

## 🔐 Security
- **Authentication/Authorization**: Verify `[Authorize]` attributes are present on sensitive controllers/actions.
- **Input Validation**: Check for `ModelState.IsValid` and proper validation logic.
- **SQL Injection**: Ensure Entity Framework or parameterized queries are used; avoid raw string concatenation for SQL.
- **Sensitive Data**: Ensure passwords or API keys are not hardcoded.

## 🚀 Performance
- **Asynchronous Programming**: Use `async`/`await` for I/O bound operations to prevent thread pool exhaustion.
- **Data Fetching**: Avoid N+1 query problems. Use `.Include()` efficiently in EF.
- **Pagination**: Large datasets should be paginated, not returned in full.

## 🧹 Code Quality
- **Naming Conventions**: Follow PascalCase for classes/methods and camelCase for local variables.
- **Error Handling**: Use global exception filters or middleware rather than scattered try-catch blocks.
- **Logging**: Ensure meaningful logging is implemented for critical paths and errors.
