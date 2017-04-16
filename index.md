Bibliothēca is a web application which can show Markdown files from projects as a html pages. Whole idea is very similar to ReadTheDocs however application is created in C# (.NET Core applications).

## Screenshots

![Screen main](images/screen01.png) ![Screen documentation](images/screen02.png)

## Architecture

Application is diviaded for a few microservices. Most of the application was created as a ASP.NET Core 1 Web application. Client application is Angular 2 application.

![Main page](images/architecture.png)

## Continuous Integration

### Services

{: .table .table-striped}
| project                                                                                                                     | branch  | status                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bibliotheca.Server.Gateway](https://github.com/BibliothecaTeam/Bibliotheca.Server.Gateway)                                 | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-gateway/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-gateway/branch/master)                                   |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-gateway/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-gateway/branch/develop)                                 |
| [Bibliotheca.Server.Indexer.AzureSearch](https://github.com/BibliothecaTeam/Bibliotheca.Server.Indexer.AzureSearch)         | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-indexer-azuresearch/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-indexer-azuresearch/branch/master)           |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-indexer-azuresearch/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-indexer-azuresearch/branch/develop)         |
| [Bibliotheca.Server.Indexer.Nightcrawler](https://github.com/BibliothecaTeam/Bibliotheca.Server.Indexer.Nightcrawler)       | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-indexer-nightcrawler/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-indexer-nightcrawler/branch/master)         |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-indexer-nightcrawler/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-indexer-nightcrawler/branch/develop)       |
| [Bibliotheca.Server.Depository.AzureStorage](https://github.com/BibliothecaTeam/Bibliotheca.Server.Depository.AzureStorage) | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-depository-azurestorage/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-depository-azurestorage/branch/master)   |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-depository-azurestorage/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-depository-azurestorage/branch/develop) |
| [Bibliotheca.Server.Depository.FileSystem](https://github.com/BibliothecaTeam/Bibliotheca.Server.Depository.FileSystem)     | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-depository-filesystem/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-depository-filesystem/branch/master)       |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-depository-filesystem/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-depository-filesystem/branch/develop)     |
| [Bibliotheca.Server.Mvc.Middleware](https://github.com/BibliothecaTeam/Bibliotheca.Server.Mvc.Middleware)                   | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-mvc-middleware/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-mvc-middleware/branch/master)                     |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-mvc-middleware/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-mvc-middleware/branch/develop)                   |
| [Bibliotheca.Server.ServiceDiscovery](https://github.com/BibliothecaTeam/Bibliotheca.Server.ServiceDiscovery)               | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-servicediscovery/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-servicediscovery/branch/master)                 |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-servicediscovery/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-servicediscovery/branch/develop)               |
| [Bibliotheca.Server.SourceControl.GitWitcher](https://github.com/BibliothecaTeam/Bibliotheca.Server.SourceControl.GitWitcher) | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-sourcecontrol-gitwitcher/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-sourcecontrol-gitwitcher/branch/master)      |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-sourcecontrol-gitwitcher/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-sourcecontrol-gitwitcher/branch/develop)    |
| [Bibliotheca.Server.Authorization.Heimdall](https://github.com/BibliothecaTeam/Bibliotheca.Server.Authorization.Heimdall)   | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-authorization-heimdall/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-authorization-heimdall/branch/master)     |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-authorization-heimdall/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-authorization-heimdall/branch/develop)   |

### Libraries

{: .table .table-striped}
| project                                                                                                                     | branch  | status                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bibliotheca.Server.Mvc.Middleware](https://github.com/BibliothecaTeam/Bibliotheca.Server.Mvc.Middleware)                   | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-mvc-middleware/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-mvc-middleware/branch/master)                     |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-mvc-middleware/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-mvc-middleware/branch/develop)                   |
| [Bibliotheca.Server.ServiceDiscovery](https://github.com/BibliothecaTeam/Bibliotheca.Server.ServiceDiscovery)               | master  | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-servicediscovery/master.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-servicediscovery/branch/master)                 |
|                                                                                                                             | develop | [![Build status](https://img.shields.io/appveyor/ci/marcinczachurski/bibliotheca-server-servicediscovery/develop.svg)](https://ci.appveyor.com/project/marcinczachurski/bibliotheca-server-servicediscovery/branch/develop)               |


## Nugets

{: .table .table-striped}
| assembly                                          | nuget                                                                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bibliotheca.Server.Mvc.Middleware.Authorization   | [![Nuget](https://img.shields.io/nuget/v/Bibliotheca.Server.Mvc.Middleware.Authorization.svg)](https://www.nuget.org/packages/Bibliotheca.Server.Mvc.Middleware.Authorization/)     |
| Bibliotheca.Server.Mvc.Middleware.Diagnostics     | [![Nuget](https://img.shields.io/nuget/v/Bibliotheca.Server.Mvc.Middleware.Diagnostics.svg)](https://www.nuget.org/packages/Bibliotheca.Server.Mvc.Middleware.Authorization/)       |
| Bibliotheca.Server.ServiceDiscovery.ServiceClient | [![Nuget](https://img.shields.io/nuget/v/Bibliotheca.Server.ServiceDiscovery.ServiceClient.svg)](https://www.nuget.org/packages/Bibliotheca.Server.ServiceDiscovery.ServiceClient/) |

## Getting started

To run application lcally you have to configure few environment variables. All of them are described below.



### Service discovery


