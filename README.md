# builds

| **Projects**                                                                                            | Status                                                                                                                                                                                                    | Packages                                                                      | Actions                                                                                   |
| ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| [Sundew.Base](https://github.com/sundews/Sundew.Base)                                                   | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Base/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                          | ![Nuget](https://img.shields.io/nuget/v/Sundew.Base)                          | [GitHub Actions](https://github.com/sundews/Sundew.Base/actions)                          |
| [Sundew.Injection](https://github.com/sundews/Sundew.Injection)                                         | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Injection/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                     | ![Nuget](https://img.shields.io/nuget/v/Sundew.Injection)                     | [GitHub Actions](https://github.com/sundews/Sundew.Injection/actions)                     |
| [Sundew.CommandLine](https://github.com/sundews/Sundew.CommandLine)                                     | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.CommandLine/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                   | ![Nuget](https://img.shields.io/nuget/v/Sundew.CommandLine)                   | [GitHub Actions](https://github.com/sundews/Sundew.CommandLine/actions)                   |
| [Sundew.DiscriminatedUnions](https://github.com/sundews/Sundew.DiscriminatedUnions)                     | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.DiscriminatedUnions/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)           | ![Nuget](https://img.shields.io/nuget/v/Sundew.DiscriminatedUnions)           | [GitHub Actions](https://github.com/sundews/Sundew.DiscriminatedUnions/actions)           |
| [Sundew.Packaging.Publish/Tool](https://github.com/sundews/Sundew.Packaging)                            | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Packaging/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                     | ![Nuget](https://img.shields.io/nuget/v/Sundew.Packaging.Publish)             | [GitHub Actions](https://github.com/sundews/Sundew.Packaging/actions)                     |
| [CommandlineBatcher](https://github.com/sundews/CommandlineBatcher)                                     | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/CommandlineBatcher/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                   | ![Nuget](https://img.shields.io/nuget/v/CommandlineBatcher)                   | [GitHub Actions](https://github.com/sundews/CommandlineBatcher/actions)                   |
| [Sundew.Generator](https://github.com/sundews/Sundew.Generator)                                         | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Generator/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                     | ![Nuget](https://img.shields.io/nuget/v/Sundew.Generator)                     | [GitHub Actions](https://github.com/sundews/Sundew.Generator/actions)                     |
| [Sundew.Quantities](https://github.com/sundews/Sundew.Quantities)                                       | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Quantities/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                    | ![Nuget](https://img.shields.io/nuget/v/Sundew.Quantities)                    | [GitHub Actions](https://github.com/sundews/Sundew.Quantities/actions)                    |
| [Sundew.Testing](https://github.com/sundews/Sundew.Testing)                                             | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Testing/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                       | ![Nuget](https://img.shields.io/nuget/v/Sundew.Testing)                       | [GitHub Actions](https://github.com/sundews/Sundew.Testing/actions)                       |
| [TransparentMoq](https://github.com/sundews/Sundew.Reactive)                                             | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/Sundew.Reactive/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                       | ![Nuget](https://img.shields.io/nuget/v/Sundew.Reactive)                       | [GitHub Actions](https://github.com/sundews/Sundew.Reactive/actions)                       |
| [TransparentMoq](https://github.com/sundews/TransparentMoq)                                             | ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/sundews/TransparentMoq/.github/workflows/dotnet.yml?branch=main&label=GitHub%20Actions&logo=github)                       | ![Nuget](https://img.shields.io/nuget/v/TransparentMoq)                       | [GitHub Actions](https://github.com/sundews/TransparentMoq/actions)                       |


### Repository Dependencies
```mermaid
flowchart RL

subgraph spp [Sundew.Packaging.Publish]
end

subgraph sd [Sundew.DiscriminatedUnions]
end

subgraph sb [Sundew.Base]
end

subgraph sc [Sundew.CommandLine]
end

subgraph cb [CommandlineBatcher]
end

subgraph sg [Sundew.Generator]
end

subgraph sq [Sundew.Quantities]
end

subgraph tm [TransparentMoq]
end

subgraph si [Sundew.Injection]
end

subgraph sr [Sundew.Reactive]
end

sb--runtime-->sd
sg--runtime-->sb
sq--runtime-->sb
spp--runtime-->sb
sr--runtime-->sb
cb--runtime-->sc--runtime-->sb

sq-.development.->sg
si-.development.->spp
sd-.development.->spp
sd-.development.->sb
sb-.development.->spp
sc--runtime---spp
sc-.development.->spp
cb-.development.->spp
sg-.development.->spp
sq-.development.->spp
tm-.development.->spp
si-.development.->sb
si-.development.->sg

linkStyle 0 color:blue;
```

