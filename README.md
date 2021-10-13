# skinet-api
I'm buidling a full-stack web application called skinet. Here is the back-end part built by .NET 5

## Here gonna be the memo how I created the project
```
// create solution file
dotnet new sln

// create webapi project using dotnet cli
dotnet new webapi -o API

// add project to the solution file
dotnet sln add API/

// create new class libraries and add them to solution file
cd ..
dotnet new classlib -o Core
dotnet new classlib -o Infrastructure
dotnet sln add Core/
dotnet sln add Infrastructure/

// connect API with Infrastructure
cd API/
dotnet add reference ../Infrastructure/
cd ..

// connect Core with Infrastructure
cd Infrastructure/
dotnet add reference ../Core/
cd ..

// save changes and build project to check if there is any error
dotnet restore
dotnet build
```
