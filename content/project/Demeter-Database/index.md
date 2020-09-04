---
title: Demeter Database
summary: A tiny relational database similar to MySQL.
date: "2020-05-01T00:00:00Z"
external_link: ""

image:
  caption: Yudai Chen
  focal_point: Smart
  
slides: example
---
+ DemeterDB is a local relational database system which provides the basic functionalities similar to a modern relational database system (MySQL, Microsoft SQL Server, etc.).、
+ Developed the database system from scratch, with LRU cached buffer manager, record manager and B+ tree file organization.

+ Built a Flex-Bison SQL compiler and a RA optimizer to support SQL Semantic check and generate optimal executable plans.
+ Implemented a two-phase multi-way merge sort over records as the primary sorting algorithm in the database system. 