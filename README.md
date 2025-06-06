# Gen AI Workshop
This AI Workshop goal is to try different AI tools for software development with different approaches 
and learn how to be more productive. 

## Prerequisites
* Create accounts at ChatGPT and Claude
* Install JetBrains Junie and Activate it
* Install VS Code and GitHub Copilot
* Install Cursor
* Install Windsurf

## Recommended Reading
* How to write better prompts
* How to use guidelines ([junie guidelines](https://github.com/JetBrains/junie-guidelines)) or 
  rules ([cursor rules](https://docs.cursor.com/context/rules), 
  [windsurf rules](https://windsurf.com/editor/directory)) with AI Agents.


## Build URL Shortener Application

* Create a short_url from a given original url
* show a list of all short_urls
* Accessing short_url should redirect to the original url 

## Tasks
* Build a fullstack url_shortener app
* Build a REST API for url_shortener
* Build an SPA for url_shortener

## Approaches
* Build the entire app with a single prompt
* Build the app with multiple prompts step-by-step
* Generate a plan and build app task-by-task

## Prompts

1. Prompt#1

> Build URL Shortener application using Java and Spring Boot

2. Prompt#2

> Build URL Shortener application with the following features:
> * Create a short_url from a given original url with 6-char length alphanumeric short_key
> * show a list of all short_urls
> * Accessing short_url should redirect to the original url
> 
> Use the following tech stack:
> * Java, Spring Boot
> * H2 database, Spring Data JPA
> * Thymeleaf, Bootstrap CSS


3. Prompt#3

> Generate a plan to build URL Shortener application with the following features:
> * Create a short_url from a given original url with 6-char length alphanumeric short_key
> * show a list of all short_urls
> * Accessing short_url should redirect to the original url
>
> Tech stack:
> * Java, Spring Boot
> * H2 database, Spring Data JPA
> * Thymeleaf, Bootstrap CSS
 
Write the plan to `plan.md` file with each task as a todo item.

Follow-up prompt:

> * Build URL Shortener application following the plan in `plan.md` file.
> * After each task is done, mark that task as Done in `plan.md` file.
> * Implement all the tasks mentioned in the `plan.md` file.


4. Prompt#4

> Build a REST API for URL Shortener application with the following features:
> * Create a short_url from a given original url with 6-char length alphanumeric short_key
> * show a list of all short_urls
> * Accessing short_url should redirect to the original url

Implement the following REST API endpoints:
 
1. Create Short URL

```shell
 POST http://localhost:8080/api/shorturls
 
 Request Payload:
 {
    "title": "Mastering Spring Boot in 5 Stages",
    "originalUrl": "https://www.sivalabs.in/mastering-spring-boot-in-5-stages/"
 }
 
 Response:
 {
    "shortUrl": "http://localhost:8080/s/{shortKey}"
 }
 
```

2. Get All Short URLs

```shell
 GET http://localhost:8080/api/shorturls
 
 Response:
 [
     {
        "title": "Mastering Spring Boot in 5 Stages",
        "shortUrl": "http://localhost:8080/s/{shortKey}"
     },
     {
        "title": "Spring Boot + Testcontainers Tests at Jet Speed",
        "shortUrl": "http://localhost:8080/s/{shortKey}"
     },
     ...
     ...
 ]
 
```


3. Redirect Short URL to Original URL

```shell
 GET http://localhost:8080/s/{shortKey}
 
 Response:
 HTTP Status Code: 301
 Header: Location: {originalUrl}
```

> Use the following tech stack:
> * Java, Spring Boot
> * H2 database, Spring Data JPA

5. Prompt#5

Add guidelines and use prompt#4.

