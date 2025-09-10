## Coming Soon

# Library App

## Description

Library App is a modular, test-driven library management system built with .NET 8.0 and C#. It provides a console-based interface for searching patrons, managing book loans, and renewing memberships. The application uses JSON files for data persistence and is organized into core, infrastructure, and console layers, with comprehensive unit tests.

## Project Structure

- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
      - Author.cs
      - Book.cs
      - BookItem.cs
      - Patron.cs
      - Loan.cs
    - Enums/
      - MembershipRenewalStatus.cs
      - LoanReturnStatus.cs
      - LoanExtensionStatus.cs
      - EnumHelper.cs
    - Interfaces/
      - IPatronRepository.cs
      - IPatronService.cs
      - ILoanRepository.cs
      - ILoanService.cs
    - Services/
      - PatronService.cs
      - LoanService.cs
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
      - JsonData.cs
      - JsonPatronRepository.cs
      - JsonLoanRepository.cs
  - Library.Console/
    - Library.Console.csproj
    - Program.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - CommonActions.cs
    - appSettings.json
    - Json/
      - Authors.json
      - Books.json
      - BookItems.json
      - Patrons.json
      - Loans.json
- tests/
  - UnitTests/
    - UnitTests.csproj
    - PatronFactory.cs
    - LoanFactory.cs
    - ApplicationCore/
      - PatronService/
        - RenewMembership.cs
      - LoanService/
        - ExtendLoan.cs
        - ReturnLoan.cs

## Key Classes and Interfaces

- **Entities**
  - `Author`, `Book`, `BookItem`, `Patron`, `Loan`: Core domain models representing library data.
- **Enums**
  - `MembershipRenewalStatus`, `LoanReturnStatus`, `LoanExtensionStatus`: Status codes for business operations.
  - `EnumHelper`: Utility for enum descriptions.
- **Interfaces**
  - `IPatronRepository`, `ILoanRepository`: Abstractions for data access.
  - `IPatronService`, `ILoanService`: Abstractions for business logic.
- **Services**
  - `PatronService`: Handles patron membership operations.
  - `LoanService`: Handles loan extension and return logic.
- **Infrastructure**
  - `JsonData`: Loads and saves data from JSON files.
  - `JsonPatronRepository`, `JsonLoanRepository`: JSON-backed repository implementations.
- **Console**
  - `ConsoleApp`: Main console UI state machine.
  - `ConsoleState`, `CommonActions`: Enums for UI state and actions.

## Usage

1. **Build the project:**
   ```sh
   dotnet build
