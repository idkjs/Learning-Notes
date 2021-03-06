# SQL

* [Common SQL Clauses and Their Equivalents in Java 8 Streams](https://blog.jooq.org/2015/08/13/common-sql-clauses-and-their-equivalents-in-java-8-streams/)
* [Periscope Data Blog](https://www.periscopedata.com/blog/)
* [Modern SQL](http://modern-sql.com/)
* [What is the best online resource to learn advanced SQL?](https://news.ycombinator.com/item?id=13417326)
* [Cool queries](https://github.com/sagemathinc/cocalc/blob/master/src/scripts/postgresql/cool-queries.md)
* [**How To Write Better Queries**](https://www.datacamp.com/community/tutorials/sql-tutorial-query)
* [How To Write Better SQL Queries: The Definitive Guide – Part 1](http://www.kdnuggets.com/2017/08/write-better-sql-queries-definitive-guide-part-1.html/2)
* [Finding the Oldest/Youngest Records Within a Group](https://robots.thoughtbot.com/ordering-within-a-sql-group-by-clause)

## JOOQ

* [Top 10 SQL Dialect Emulations Implemented in jOOQ](https://blog.jooq.org/2018/03/13/top-10-sql-dialect-emulations-implemented-in-jooq/)

## SQL Injection

* [SQL Injection Wiki](https://sqlwiki.netspi.com/)
* [Payloads All The Things](https://github.com/swisskyrepo/PayloadsAllTheThings)

## Index

## Query

```sql
# Shorthand for >= AND <= (both inclusive)
WHERE price BETWEEN 10 AND 20
```

## Subquery

Always go for CTE and only when it become a performance issues, then go for subquery.

* [Use Subqueries to Count Distinct 50X Faster](https://www.periscopedata.com/blog/use-subqueries-to-count-distinct-50x-faster.html)

## Grouping

* [What You Need To Know About SQL's Group By](https://periscopedata.com/blog//everything-about-group-by.html)

When you do aggregate function, you can't access the result at the WHERE clause, because WHERE clause is already logically executed.

> If you're grouping by a column, it simple does not make sense to also aggregate that column.

## Functional Dependency

* [MySQL 5.7.5: GROUP BY respects functional dependencies](https://rpbouman.blogspot.sg/2014/09/mysql-575-group-by-respects-functional.html)

## Joins

The SQL standard introduces "noise words" in the syntax, and both inner and outer are noise words: a *left*, *right* or *full* join is always an **outer** join, and a straight join always is an **inner** join.

* [**Can we stop with the SQL JOINs Venn diagrams insanity?**](https://towardsdatascience.com/can-we-stop-with-the-sql-joins-venn-diagrams-insanity-16791d9250c3)
* [Keep INNER JOIN when merging relations](https://github.com/rails/rails/pull/27063)
* [Visual Representation of SQL Joins](https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins)

## Aggregate

It is important to understand the interaction between aggregates and SQL's WHERE and HAVING clauses. The fundamental difference between WHERE and HAVING is this: WHERE selects input rows before groups and aggregates are computed (thus, it controls which rows go into the aggregate computation), whereas HAVING selects group rows after groups and aggregates are computed. Thus, the WHERE clause must not contain aggregate functions; it makes no sense to try to use an aggregate to determine which rows will be inputs to the aggregates. On the other hand, the HAVING clause always contains aggregate functions. (Strictly speaking, you are allowed to write a HAVING clause that doesn't use aggregates, but it's seldom useful. The same condition could be used more efficiently at the WHERE stage.)

* Most aggregate functions ignore `null` inputs, so that rows in which one or more of the expressions yield `null` are discarded.

```sql
count(*) -- Total number of input rows
count(f1) -- Number of input rows in which f1 is non-null
count(distinct f1) -- Number of distinct non-null values of f1
```

## Entity Attribute Value - EAV

* [Pivot — Rows to Columns](https://modern-sql.com/use-case/pivot)

## Videos

* [How Modern SQL Databases Come up with Algorithms that You Would Have Never Dreamed Of](https://www.youtube.com/watch?v=wTPGW1PNy_Y)


