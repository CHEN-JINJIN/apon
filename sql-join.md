
# 连接查询

## INNER JOIN

>内连接，返回在两张表中具有匹配值的记录

```sql
SELECT column_names FROM table1 INNER JOIN table2 ON table1.column_name=table2.column_name;
SELECT table1.column_name1, table2.column_name2, table3.column_name3 FROM ((table1 INNER JOIN table2 ONrelationship) INNER JOIN table3 ON relationship);
```

## LEFT (OUTER) JOIN

>左外连接，返回左表（table1）中的所有记录，以及右表中的匹配记录（table2）

```sql
SELECT column_names FROM table1 LEFT JOIN table2 ON table1.column_name=table2.column_name;
```

## RIGHT (OUTER) JOIN

>右外连接，返回右表（table2）中的所有记录，以及左表（table1）中匹配的记录

```sql
SELECT column_names FROM table1 RIGHT JOIN table2 ON table1.column_name=table2.column_name;
```

## FULL (OUTER) JOIN

>全外连接，全连接是左右外连接的并集. 连接表包含被连接的表的所有记录, 如果缺少匹配的记录, 以 NULL 填充

```sql
SELECT column_names FROM table1 FULL OUTER JOIN table2 ON table1.column_name=table2.column_name;
```

## Self JOIN

>自连接，表自身连接

```sql
SELECT column_names FROM table1 T1, table1 T2 WHERE condition;
```
