# acc-scheduler

## Tech Framework
    * Dot Net Core 3.1
    * Sql Server 2017
    * Rabbit MQ

## Development Packages 

    [AutoMapper.Extensions.Microsoft.DependencyInjection8.1.0](https://www.nuget.org/packages/AutoMapper.Extensions.Microsoft.DependencyInjection/)
    * [Fluentvalidation.Aspnetcore 9.3.0](https://www.nuget.org/packages/FluentValidation.AspNetCore/)
    * [Microsoft.EntityFrameworkCore.SqlServer 5.0.0](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/5.0.0)
    * [NewtonSoft.Json 12.0.3](https://www.nuget.org/packages/Newtonsoft.Json/)

## Project Structure
    ..
    ├── Scheduler.BackgroundWorker          # Service worker to check for incoming create/Update/delete requests from webapi for schedules
    ├── Scheduler.Business                  # Logical layer that takes care of mapping configurations from webapi to data layer
    ├── Scheduler.Common                    # Common libraries used across entire project
    ├── Scheduler.Data                      # Peristence layer for incoming requests
    ├── Scheduler.WebApi                    # ASP.NET WebApi service for HTTP calls
    ├── Scheduler.Scripts                   # Database scripts 
    
    Tests
    ..
    ├── Scheduler.BackgroundWorker.Tests 
    ├── Scheduler.Business.Tests            
    ├── Scheduler.Data.Tests                
    ├── Scheduler.WebApi.Tests              
    
    API Specification & Readme
    ..
    ├── scheduler-api-spec.yml              # Swagger API sepification
    └── README.md                           

## Tests

### Packages
    Unit test framework used is xunit along with below packages:

    * [FluentAssertions.AspNetCore.Mvc 3.2.0](https://www.nuget.org/packages/FluentAssertions.AspNetCore.Mvc/)
    * [Moq 4.15.2](https://www.nuget.org/packages/moq/)
    
### Test Cases execution
    Navigate to root folder and run below command. Make sure [dotnet sdk](https://docs.microsoft.com/en-us/dotnet/core/sdk) is installed

        ``` dotnet test ```


## Database Schema
    Create table schema structure using script :  [Scheduler.Scripts\CreateTableStructure.Sql](..\Scheduler.Scripts\CreateTableStructure.Sql)

