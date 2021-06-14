list:
	docker run --rm -v $(pwd):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new -l
.NOPHONY: list

new-help:
	docker run --rm -v $(PWD):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new -h
.NOPHONY: new-help

new:
	docker run --rm -v $(PWD):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet new console -n hello-world -o /app
#docker run --rm -v $(pwd):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet $@ $(0)
#docker run --rm -v ${PWD}:/docs orbyt-technical-docs:latest $(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
.NOPHONY: new

build:
	docker run --rm -v $(PWD):/app -w /app mcr.microsoft.com/dotnet/sdk:5.0 dotnet build -o /app/out -r linux-x64 --no-incremental -v d
.NOPHONY: build

package:
	docker build -t hello-world-csharp .
.NOPHONY: package
