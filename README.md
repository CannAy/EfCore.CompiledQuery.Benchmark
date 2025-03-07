# EfCore.CompiledQuery.Benchmark

This project benchmarks the performance of compiled queries in Entity Framework Core using .NET 7. It leverages `BenchmarkDotNet` for benchmarking and `Bogus` for generating fake data.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Benchmarks](#benchmarks)
- [Contributing](#contributing)
- [License](#license)

## Installation
                            
1. Clone the repository:

        git clone https://github.com/CannAy/EfCore.CompiledQuery.Benchmark.git
        cd EfCore.CompiledQuery.Benchmark
    
2. Ensure you have .NET 7 SDK installed. You can download it from the [official .NET website](https://dotnet.microsoft.com/download/dotnet/7.0).

3. Restore the project dependencies:
    
## Usage

1. Update the connection string in `AppDbContext.cs` to point to your SQL Server instance:

        optionsBuilder.UseSqlServer(@"Your_Connection_String_Here");
        dotnet restore
          
2. Run the benchmarks:

        dotnet run -c Release
    
## Project Structure

- **EfCore.CompiledQuery.Benchmark.csproj**: Project file containing dependencies and target framework.
- **AppDbContext.cs**: Entity Framework Core DbContext setup with compiled and non-compiled query methods.
- **Customer.cs**: Entity class representing the Customer table.
- **Program.cs**: Entry point for the application, setting up and running benchmarks.

### AppDbContext.cs

This file contains the `AppDbContext` class which is responsible for configuring the database context and seeding data using `Bogus`.

## Benchmarks

The project uses `BenchmarkDotNet` to measure the performance of compiled vs non-compiled queries. The results will be displayed in the console after running the benchmarks.


