list:
	docker run --rm -v $(pwd):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new -l
.NOPHONY: list

new-help:
	docker run --rm -v $(PWD):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new -h
.NOPHONY: new-help

new:
	docker run --rm -v $(PWD):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new console -n hello-world -o /app
.NOPHONY: new

build:
	docker build -t hello-world-csharp .
.NOPHONY: build
