+++
pre = "<b>3.6. </b>"
title = "Test Engine"
weight = 6
chapter = true
+++

ShardingSphere provided a full functionality test engine. it defines SQLs in xml files, every single SQL is drove by SQL parse unit test engine and integration test engine,
each engine is suit for H2、MySQL、PostgreSQL、SQLServer and Oracle

The SQL parsing unit test covers both SQL placeholder and literal dimension. 
Integration test can be further divided into two dimensions of strategy and JDBC; the former one includes strategies as Sharding, table Sharding, database Sharding, and read-write split while the latter one includes `Statement` and `PreparedStatement`.

Therefore, one SQL can drive 5 kinds of database parsing * 2 kinds of parameter transmission modes + 5 kinds of databases * 5 kinds of Sharding strategies * 2 kinds of JDBC operation modes = 60 test cases, to enable ShardingSphere to achieve the pursuit of high quality.

> whenever describe the sub-path under a specific path, there may be more than one, here represent SQL-TYPE and SHARDING-TYPE as following :
>
>SQL-TYPE : is one of or collection of dal,dcl，ddl，dml，dql，tcl
>
>SHARDING-TYPE : is one of or collection of db，dbtbl_with_masterslave，masterslave，tbl
