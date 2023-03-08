# builds

| **Projects**                                                                                            | Status                                                                                                                                                        | Packages                                                                      | Actions                                                                                   |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| [Sundew.Base](https://github.com/sundews/Sundew.Base)                                                   | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.Base/.github/workflows/dotnet.yml?branch=main)                          | ![Nuget](https://img.shields.io/nuget/v/Sundew.Base)                          | [GitHub Actions](https://github.com/sundews/Sundew.Base/actions)                          |
| [Sundew.DiscriminatedUnions](https://github.com/sundews/Sundew.DiscriminatedUnions)                                                   | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.DiscriminatedUnions/.NET?label=GitHub%20Actions&logo=github)                          | ![Nuget](https://img.shields.io/nuget/v/Sundew.DiscriminatedUnions)                          | [GitHub Actions](https://github.com/sundews/Sundew.DiscriminatedUnions/actions)                          |
| [Sundew.CommandLine](https://github.com/sundews/Sundew.CommandLine)                                     | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.CommandLine/.NET?label=GitHub%20Actions&logo=github)                   | ![Nuget](https://img.shields.io/nuget/v/Sundew.CommandLine)                   | [GitHub Actions](https://github.com/sundews/Sundew.CommandLine/actions)                   |
| [Sundew.DiscriminatedUnions](https://github.com/sundews/Sundew.DiscriminatedUnions)                     | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.DiscriminatedUnions/.NET?label=GitHub%20Actions&logo=github)           | ![Nuget](https://img.shields.io/nuget/v/Sundew.DiscriminatedUnions)           | [GitHub Actions](https://github.com/sundews/Sundew.DiscriminatedUnions/actions)           |
| [Sundew.Packaging.Publish/Tool](https://github.com/sundews/Sundew.Packaging)                            | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.Packaging/.NET?label=GitHub%20Actions&logo=github)                     | ![Nuget](https://img.shields.io/nuget/v/Sundew.Packaging.Publish)             | [GitHub Actions](https://github.com/sundews/Sundew.Packaging/actions)                     |
| [CommandlineBatcher](https://github.com/sundews/CommandlineBatcher)                                     | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/CommandlineBatcher/.NET?label=GitHub%20Actions&logo=github)                   | ![Nuget](https://img.shields.io/nuget/v/CommandlineBatcher)                   | [GitHub Actions](https://github.com/sundews/CommandlineBatcher/actions)                   |
| [Sundew.Generator](https://github.com/sundews/Sundew.Generator)                                         | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.Generator/.NET?label=GitHub%20Actions&logo=github)                     | ![Nuget](https://img.shields.io/nuget/v/Sundew.Generator)                     | [GitHub Actions](https://github.com/sundews/Sundew.Generator/actions)                     |
| [Sundew.Quantities](https://github.com/sundews/Sundew.Quantities)                                       | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.Quantities/.NET?label=GitHub%20Actions&logo=github)                    | ![Nuget](https://img.shields.io/nuget/v/Sundew.Quantities)                    | [GitHub Actions](https://github.com/sundews/Sundew.Quantities/actions)                    |
| [Sundew.TextView.ApplicationFramework](https://github.com/sundews/Sundew.TextView.ApplicationFramework) | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/Sundew.TextView.ApplicationFramework/.NET?label=GitHub%20Actions&logo=github) | ![Nuget](https://img.shields.io/nuget/v/Sundew.TextView.ApplicationFramework) | [GitHub Actions](https://github.com/sundews/Sundew.TextView.ApplicationFramework/actions) |
| [TransparentMoq](https://github.com/sundews/TransparentMoq)                                             | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/sundews/TransparentMoq/.NET?label=GitHub%20Actions&logo=github)                       | ![Nuget](https://img.shields.io/nuget/v/TransparentMoq)                       | [GitHub Actions](https://github.com/sundews/TransparentMoq/actions)                       |


### Repository Dependencies
```mermaid
flowchart RL

subgraph spp[Sundew.Packaging.Publish]
end

subgraph sd[Sundew.DiscriminatedUnions]
end

subgraph sb[Sundew.Base]
end

subgraph sc[Sundew.CommandLine]
end

subgraph cb[CommandlineBatcher]
end

subgraph sg[Sundew.Generator]
end

subgraph sq[Sundew.Quantities]
end
subgraph tm[TransparentMoq]
end

sd--metadata-->sb
sb--runtime-->sd
sg--runtime-->sb
sg--runtime-->sc
sq--runtime-->sb
spp--runtime-->sb
cb--runtime-->sc--runtime-->sb

sq-.development.->sg
sd-.development.->spp
sb-.development.->spp
sc<--runtime---spp
sc-.development.->spp
cb-.development.->spp
sg-.development.->spp
sq-.development.->spp
tm-.development.->spp

linkStyle 0 color:blue;
```

