# Jobspec

## Context
Our team's expertise is mainly concentrated around opentext cms.

2 years ago I started working on a project which purpose was to provide the same features we're offering on OT's platform but for Sharepoint Online.

Our document processing provides a lot of features like:
- document conversion to Word, PDF or HTML
- dynamic metadata insertion
- applying headers and footers
- watermarking
- generating Table of Contents from PDF bookmarks and Word TOCs
- merging documents

We manage more than 200 document input formats.

At that time, I made some choices about which architecture and which tech stack I would use to build this project. 

I didn't adopt the "start small and scale later" approach. 

I was concerned about the fact that we should be able to manage a lot of documents and a lot of users.

That lead me to choose k8s as a container orchestrator and to use a microservices architecture.

For the conception I had to think about the following points among others:
- how to manage authentication and authorization 
- how to manage the document processing workflow
- how to keep documents secured and encrypted while being able to process them

The conception lead to the development of a minimal viable product which is not in production.

We have selected a few customers and partners who are excited about the product to beta test it and provide feedback.

## Perimeter
The job concerns the Sharepoint Online project we named DocumentFactory.

The project is composed of the following parts:
- a web application built with Angular to manage user settings and document process definitions
- backend services to manage documents processing, mostly built with golang and .Net Core
- a Sharepoint webpart component built with Angular to display document processing objects (which we call Document Builders) and to allow users to interact with them.

The project is deployed on a k8s cluster hosted on GKE.

The job perimeter is the backend services part.

## Expectations
We need someone who is able to learn and understand the project's architecture.

I don't think it is necessary to have a knowledge of document formats or Sharepoint. Sharepoint is just a document repository, and we made DocumentFactory to be able to process documents from any repo, including Content Server, DropBox, GitHub, a filesystem or ftp.

We expect someone to be able to understand the different roles of our software architecture components, to then be able to explain them, to document them and finally to improve them.
