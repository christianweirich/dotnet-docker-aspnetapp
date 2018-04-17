# ASP.NET Core Docker app

## Prerequisits

To build and run, install the following items:

- [.NET Core SDK 2.0](https://www.microsoft.com/net/core) or later
- [Docker 17.06](https://docs.docker.com/release-notes/docker-ce/) or later
- Git

## Run the ASP.NET app locally

You can build and run the application locally with the .NET Core 2.0 SDK using the following commands (The instructions assume the root of the repository):

```bash
cd aspnetapp
dotnet run
```
After the application starts, visit http://localhost:5000 in your web browser.

## Build and run the sample with Docker for Linux containers

You can build and run the sample in Docker using Linux containers using the following commands (The instructions assume the root of the repository):

```bash
cd aspnetapp
docker build -t aspnetapp .
docker run -it --rm -p 5000:80 --name aspnetcore_sample aspnetapp
```
After the application starts, visit http://localhost:5000 in your web browser.

>The `docker run` '-p' argument maps port 5000 on your local machine to port 80 in the container (the port mapping form is host:container). For more information, see the docker run reference on command-line parameters.

## Docker Images used in this sample

The following Docker images are used in this sample

- `microsoft/aspnetcore-build:2.0`
- `microsoft/aspnetcore:2.0`

---
Reference:
https://docs.microsoft.com/en-us/dotnet/core/docker/building-net-docker-images