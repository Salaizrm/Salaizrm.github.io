---
layout: post
title:      "SQL and why its important"
date:       2020-04-06 20:31:43 +0000
permalink:  sql_and_why_its_important
---

SQL is a really nifty tool used to communicate and create databases. To be honest, its actaully really simple in concept when you wanna create a table simple code it like this:
```
def table_example
sql = <<-SQL
CREATE TABLE IF NOT EXISTS test (
id INTEGER PRIMARY KEY,
name TEXT,
stuff INTEGER
SQL

DB[:conn].execute(sql)
end
```

Of course you can add more columns and so on. You can also create this table straight in the terminal when activating SQL from the terminal. The "DB[:conn].execute(sql) is simply telling whatever class were putting this instance method in to execute this command into SQL and create our table. you of course will need to create the "DB[:conn]" method in a seperate file that tells SQL "this is the command that will tell SQL to insert my methods into SQL". The "=<<-SQL" is called a heredoc, an awesome tool to use to simplify this line of code. We can also create methods that allow us to search or add info to our table:

```
def find_example
sql =<<-SQL
SELECT * 
FROM test
SQL

DB[:conn].execute(sql)
end

```

Here we are telling SQL to find everything from the table "test". Thats what the " * " is, a wildcard. we can of course narrow our search by changing the wild card to find a specific column like "name" or "stuff".

SQL is important because it makes creating and searching databases extremely simple. creating commands for SQL is also really easy and if you ever need to find a specific way to ask for something from  a database a quick google search will show you a plethora of information on how to ask your database where to find something or show something.
