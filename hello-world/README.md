# Hello world csharp

This project is a playground to use .Net 5 with docker.

## Structure

* `Dockerfile` - Dockerfile with instructions to package and generate an executable .Net 5 docker image
* `hello-world.csproj` - Standard csproj file created via `dotnet new`
* `Makefile` - Makefile to execute build tasks
* `Program.cs` - Standad Program.cs file generated via `dotnet new`

## Running
The main objective of this project is to exemplify how to use docker to build and run .Net 5 application. Thus the only things you can do here is... build and execute docker containers.

### Make targets

* `make new` - Example of make task to generate a new project. It uses the `mcr.microsoft.com/dotnet/sdk:5.0` docker image to run `dotnet new` command. Since I have pushed the generated source code already, it will fail if you try to execute it
* `make build` - It uses the `Dockerfile` to build and generate a runtime docker image that will execute your program.
Although we could target an Alpine runtime environment to generate an even smaller docker image, the .Net 5 runtime plus the program generates a 186MB image which is impressive small.
* `make list` - It lists the available templates for `dotnet new`
* `make new-help` - It lists the available options for `dotnet new`

### Running the generated docker image
After building the docker image with `make build` you can execute it with:

```
  docker run --rm hello-world-csharp
```

If everything went well you should see an exciting `Hello World!` message :/