---
layout: post
title:  "Updating ISPConfig 3"
date:   2020-11-19 09:56:44 +0200
categories: ispconfig update
---
Before updating

- check the page https://www.howtoforge.com/updating-ispconfig-3-1-to-ispconfig-3-2/
- prevent MySQL errors by executing the following MySQL statement on the `dbispconfig` database:

```sql
USE dbispconfig
ALTER TABLE web_domain ROW_FORMAT=DYNAMIC;
```