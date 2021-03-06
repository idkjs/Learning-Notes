# Data Product

Big Data refers to data sets large enough (Volume) and data streams fast enough (Velocity), from heterogeneous data sources (Variety), that has outpaced our capability to store, process, analyze, and understand.

Many Big Data sources represent **series of events** that are continuously produced (e.g. tweets, web logs, user transactions, system logs, sensors).

* [Turning Data into Product](http://www.juiceanalytics.com/writing/turning-data-into-product)
* [How data analytics killed the Premier League's long ball game](https://www.wired.co.uk/article/premier-league-stats-football-analytics-prozone-gegenpressing-tiki-taka)
* [Why data science is simply the new astrology](https://www.livemint.com/Sundayapp/zDSjhU5IzcuI7ypo6W4WtL/Why-data-science-is-simply-the-new-astrology.html)
* [When your client has a data question, do you have the answer?](https://blog.data.world/when-your-client-has-a-data-question-do-you-have-the-answer-45093e9336a7)

## What do people want analytics?

* People want business insights
* How did this happen?
* What will be the future results?
* What are the new patterns and relationships in this data?

> Information is the oil of 21st century, and analytics is the combustion engine.

## Decoupled System

Download and upstream are decoupled.

```
Data Bus -> Pub Sub -> Materialized Views
```

* Immutable log - don't delete your log
* Materialized views

Amazon SQS take in transactional log (from S3), apply lambda function to produce periodic materialized views.

## Event Logs

* [Why You Should Query Your Event Logs in Hadoop](http://querytreeapp.com/blog/querying-your-event-logs-in-hadoop/)
* [The Totally Managed Analytics Pipeline: Segment, Lambda, and Dynamo](https://segment.com/blog/the-totally-managed-analytics-pipeline/)
* [Netflix: 1 trillion events a day into streaming ingestion pipeline](https://medium.com/netflix-techblog/notebook-innovation-591ee3221233)

Why we don't store logs in databases:

* Each event has different properties. If you are going to create a new table for each type of event that can become unmaintainable.
* Adding index to the table may not be advisable since the log is append-only and indexing will have performance issues.
* Without indexing, querying huge log will suffer.

## Advice

* Data is still about people
* Data itself isn't the product
* Mashup your private data with publicly available data like environment, educations, industry, etc.

## Videos

* [Big Data Architectural Patterns and Best Practices on AWS](https://www.youtube.com/watch?v=RNrsIlweCno)
* [Stream-first architecture, Apache Flink & other emerging technologies](https://www.youtube.com/watch?v=ljDTXdqej9Q)
* [Introduction to Data Science - A Practical Viewpoint--Jesus Rogel-Salazar](https://learning.oreilly.com/videos/odsc-europe-2018/9780135768389/9780135768389-ODSC_EURO18_01)

## Blog

* [MapR Blog](https://mapr.com/blog/)
* [Data Artisans](https://data-artisans.com/blog)
* [Segment Engineering Blog](https://segment.com/blog/categories/engineering/)

