---
layout: til
title: "Materialize the Query Result for Performance"
date: 2019-05-12
author: Lei Ma
comments: true
category:
- data
tag:
- Data Warehouse
- Big Query
excerpt: Materialize the query result for multistage queries to make your query faster and lower the costs.
---

Write the results to a table for multistage query it is costing to much data. 

In many operations such as row_number it will cost a lot more data than the selected columns. Writing to a destination table would save some data.

