---
name: csharp-async
description: 'Get best practices for C# programming'
---

# 🧑‍💻 Quality Criteria: CSharp Code
The CSharp Code quality criteria focus on ensuring that C# code is well-structured, maintainable, and adheres to best practices. This includes aspects such as code readability, performance, security, and adherence to coding standards.

## Metadata
| Key               | Value                             |
|-------------------|-----------------------------------|
| Id                | QC-CSHARP-CODE                    |

### Change Log
| Date       | Version | Description                     | Author        |
|------------|---------|---------------------------------|---------------|
| 2026-02-13 | 0001    | Initial creation of the document | Tirsvad      |
| 2026-03-29 | 0002    | Added Asynchronous Method Naming criteria | Tirsvad |
| 2026-04-25 | 0003    | Added TAP - Task-based Asynchronous Pattern | Tirsvad |


## Table of Contents

- [📝 General Criteria](#general-criteria)
- [📐 C# Quality Criteria](#csharp-quality-criteria)
- [🔍 Pattern Matching for C#](#pattern-matching)
  - [⚡ TAP - Task Asynchronous Programming](#tap)

<a name="general-criteria"></a>
## 📝 General Criteria
- **Encoding**: All C# files must use UTF-8 encoding without BOM (Byte Order Mark).
- **Language**: Code must be written in English, including comments, variable names, method names and class names.

<a name="csharp-quality-criteria"></a>
## 📐 C# Quality Criteria
- **Filename**: Filenames must use PascalCase and match the name of the class or interface defined in the file. For example, if the class is named `Customer`, the file must be named `Customer.cs`.
- **Readability**: Each of the members (`Fields`, `Properties`, `Methods`) should be grouped logically and placed in their own `#region`.
    - `Methods` should be grouped by functionality and include a descriptive comment.

### Naming Conventions
- **Interfaces**: Interface names must start with a capital "I" followed by a descriptive name in PascalCase (e.g., `IUserRepository`).
- **Namespaces**: Namespace names must use PascalCase and reflect the project structure (e.g., `ProjectName.Core.Services`).
- **Types**: Type names (e.g., classes, structs, enums) must use PascalCase and describe the type (e.g., `UserStatus`).
- **Attributes**: Attribute names must use PascalCase and describe the purpose of the attribute (e.g., `Required`, `MaxLength`).
- **Classes**: Class names must use PascalCase and describe the class purpose (e.g., `UserService`).
- **Parameters**: Parameter names must use camelCase and describe the purpose of the parameter (e.g., `userName`).
- **Variables**: Variable names must use camelCase and describe their purpose (e.g., `totalAmount`).
- **Private fields**: Private field names must use camelCase and start with an underscore (e.g., `_firstName`).

### Asynchronous Method Naming

- **Async Suffix**: Methods that return an awaitable type (such as `Task` or `Task<T>`) must have names ending with the `Async` suffix (e.g., `GetDataAsync`).
    - This follows Microsoft best practices and the Task-based Asynchronous Pattern (TAP).
    - The `Async` suffix provides clarity, avoids naming conflicts with synchronous methods, and improves code readability.
- **Exceptions**:
    - **Event Handlers**: Methods that are event handlers (with a `void` return type and a delegate-determined signature) should not use the `Async` suffix (e.g., `OnButtonClick`).
    - **Interface or Base Class Contracts**: If implementing an interface or base class that defines a method name, the `Async` suffix may be omitted to match the contract.
    - **Non-Awaitable Methods**: Methods that start asynchronous operations but do not return a `Task` (i.e., "fire-and-forget" methods, which are generally discouraged) should not use the `Async` suffix. Instead, use prefixes like `Begin` or `Start` (e.g., `BeginUpload`).

### Class Naming & Responsibility
- Use descriptive names; follow Single Responsibility Principle
- **Mapper**: Transforms one object to another
- **Service**: Performs operations with side effects or orchestration, may have state
- **Manager**: Methods for a context, no state outside injected classes, business logic not in domain model
- **Handler**: Responds to requests, executes business logic via other classes
- **Helper**: Static, pure functions, no state, very small

### Formatting
- Apply code-formatting style defined in `.editorconfig`.
- Prefer file-scoped namespace declarations and single-line using directives.
- Insert a newline before the opening curly brace of any code block (e.g., after `if`, `for`, `while`, `foreach`, `using`, `try`, etc.).
- Ensure that the final return statement of a method is on its own line.
- Use pattern matching and switch expressions wherever possible.
- Use `nameof` instead of string literals when referring to member names.
- Ensure that XML doc comments are created for any public APIs. When applicable, include `<example>` and `<code>` documentation in the comments.

### Nullable Reference Types
- Declare variables non-nullable, and check for `null` at entry points.
- Always use `is null` or `is not null` instead of `== null` or `!= null`.
- Trust the C# null annotations and don't add null checks when the type system says a value cannot be null.

### Code Quality
- **Method length**: Methods should not exceed 30 lines of code. If a method becomes too long, it should be split into smaller, more focused methods.
- **Comments**: Comments should be used to explain "why" something is done, not "what" is being done. Code should be as self-explanatory as possible.
- **Error handling**: Use exceptions for error handling instead of return codes. Ensure exceptions are caught and handled at appropriate locations.
- **Indentation**: Use consistent indentation with 4 spaces per level.
- **Use of `var`**: Avoid using `var`; use explicit types instead. (e.g., use `int count = 0;` instead of `var count = 0;`)

<a name="pattern-matching"></a>
## 🔍 Pattern Matching for C#
- Use pattern matching to simplify code and improve readability.

<a name="tap"></a>
### ⚡ TAP - Task Asynchronous Programming

It helps improve application responsiveness and scalability by allowing non-blocking operations, especially for I/O-bound and long-running tasks.

#### Naming Convention:

In C#, while the Task-based Asynchronous Pattern (TAP) generally recommends suffixing asynchronous methods with Async, there are specific scenarios where you should omit it.

- Non-Awaitable Return Types: If a method initiates an asynchronous operation but does not return an awaitable type (like Task or ValueTask), you should not use the Async suffix. Instead, use prefixes like Begin or Start.
- Event Handlers: Standard event handlers, such as OnButtonClick, should not be renamed even if they contain asynchronous code.
- Interface or Base Class Requirements: You should ignore the convention if an existing interface contract or base class suggests a different name that you must implement.
- Framework-Called Methods: Methods primarily called by a framework rather than directly by developers (e.g., ASP.NET Core controller actions or MediatR handlers) often omit the suffix because the awaitability is implied by the framework's architecture.
- Uniformly Asynchronous Codebases: In modern projects where nearly all operations are asynchronous, some teams choose to omit the suffix to reduce "noise," treating Async as the default state rather than the exception.
- Internal or Private Methods: Some developers consider the suffix optional for private methods within a class, as the scope is limited and the return type is easily verifiable within the same file.
- Use the 'Async' suffix for all other async methods if they return a Task or Task<T> (e.g., `GetDataAsync()`, `SaveAsync()`)
- Match method names with their synchronous counterparts when applicable (e.g., `GetDataAsync()` for `GetData()`)

#### Benefits:
- **Improved Responsiveness**: Asynchronous methods allow the application to remain responsive while performing long-running operations, such as file I/O, network requests, or database queries.
- **Scalability**: Asynchronous programming can help improve the scalability of applications by freeing up threads to handle other requests while waiting for I/O operations to complete.
- **Better Resource Utilization**: Asynchronous methods can help reduce resource contention and improve overall performance by allowing the application to make better use of available threads and system resources.
- **Enhanced User Experience**: Asynchronous programming can help create a smoother user experience by preventing the application from freezing or becoming unresponsive during long-running operations.
- **Integration with Modern C# Features**: The TAP pattern integrates well with modern C# features such as `async` and `await`, making it easier to write asynchronous code that is more readable and maintainable.
- **Error Handling**: Asynchronous methods can use `try-catch` blocks to handle exceptions, allowing for better error handling and recovery in asynchronous operations.

