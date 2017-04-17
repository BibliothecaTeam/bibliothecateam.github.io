## Architecture

Application is diviaded for a few microservices. Most of the application was created as a ASP.NET Core 1 Web application. Client application is Angular 4 application.

{: .custom-img-width}
![Main page](images/architecture.png)

Below is short description of the backend microservices:

 - *(mandatory)* **Gateway** service is responsible for whole communication between services (also is main API endpoint)
 - *(mandatory)* **Depository** service is resposible for storing Markdown files. Currently there are two implementation of that service:
   
   - **Azure storage** stores documentation on cloud storage
   - **File system** stores documentantion on local file systes

 - *(optional)* **Indexer** service is resposible for creating search index. Thanks to this we can use search by keywords in all documentation projects
 - *(optional)* **Authorization** service is resposible for storing information about user and his access
 - *(optional)* **Nightcrawler** service can reindex all documentation projects
 - *(optional)* **Git Witcher** service is responsible for downloading source codes from Git (after webhook)

Only the mandatory services are needed for basic functionality.

More information about configuration all applications you can find in [Getting started](/getting-started.html) page.
