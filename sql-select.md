# 查询数据SQL

## SELECT

>用于从表中选取数据

?>SQL语句对大小写不敏感，SELECT 等效于 select。

```sql
SELECT * FROM table_name;
```

## DISTINCT

>用于过滤掉重复的值并返回指定列的行

```sql
SELECT DISTINCT column_name;
```

## WHERE

>用于过滤记录/行

```sql
SELECT column1, column2 FROM table_name WHERE condition;
SELECT * FROM table_name WHERE condition1 AND condition2;
SELECT * FROM table_name WHERE condition1 OR condition2;
SELECT * FROM table_name WHERE NOT condition;
SELECT * FROM table_name WHERE condition1 AND (condition2 OR condition3);
SELECT * FROM table_name WHERE EXISTS (SELECT column_name FROM table_name WHERE condition);
```

## ORDER BY

>用于结果集的排序，升序（ASC）或者降序（DESC）

```sql
SELECT * FROM table_name ORDER BY column;
SELECT * FROM table_name ORDER BY column DESC;
SELECT * FROM table_name ORDER BY column1 ASC, column2 DESC;
```

## TOP

>用于指定从表顶部返回的记录数

```sql
SELECT TOP number columns_names FROM table_name WHERE condition;
SELECT TOP percent columns_names FROM table_name WHERE condition;
```

!>并非所有数据库系统都支持SELECT TOP。 MySQL 中是LIMIT子句

## LIKE

>用于搜索列中的特定模式，WHERE 子句中使用的运算符

- % (百分号) 匹配零个或多个字符的任何字符串
- _ (下划线) 匹配任何单个字符

```sql
SELECT column_names FROM table_name WHERE column_name [NOT] LIKE pattern;
```

| Field | pattern  | Description
|-------|----------|----------------------
| LIKE  | ‘a%’     | 查找任何以“a”开头的值
| LIKE  | ‘%a’     | 查找任何以“a”结尾的值
| LIKE  | ‘%or%’   | 查找任何包含“or”的值
| LIKE  | ‘_r%’    | 查找任何第二位是“r”的值
| LIKE  | ‘a_%_%’  | 查找任何以“a”开头且长度至少为3的值  
| LIKE  | ‘[a-c]%’ | 查找任何以“a”或“b”或“c”开头的值

## IN

>用于在 WHERE 子句中指定多个值的运算符
?>本质上，IN运算符是多个OR条件的简写

```sql
SELECT column_names FROM table_name WHERE column_name IN (value1, value2, …);
SELECT column_names FROM table_name WHERE column_name IN (SELECT STATEMENT);
```

## BETWEEN

>用于过滤给定范围的值的运算符

```sql
SELECT column_names FROM table_name WHERE column_name BETWEEN value1 AND value2;
SELECT * FROM Products WHERE (column_name BETWEEN value1 AND value2) AND NOT column_name2 IN (value3, value4);
SELECT * FROM Products WHERE column_name BETWEEN #01/07/1999# AND #03/12/1999#;
```

## NULL

>代表一个字段没有值

```sql
SELECT * FROM table_name WHERE column_name IS NULL;
SELECT * FROM table_name WHERE column_name IS NOT NULL;
```

## AS

>用于给表或者列分配别名

```sql
SELECT column_name AS alias_name FROM table_name;
SELECT column_name FROM table_name AS alias_name;
SELECT column_name AS alias_name1, column_name2 AS alias_name2;
SELECT column_name1, column_name2 + ‘, ‘ + column_name3 AS alias_name;
```

## UNION

>用于组合两个或者多个 SELECT 语句的结果集的运算符

- 每个 SELECT 语句必须拥有相同的列数
- 列必须拥有相似的数据类型
- 每个 SELECT 语句中的列也必须具有相同的顺序

```sql
SELECT columns_names FROM table1 UNION SELECT column_name FROM table2;
```

!>UNION 仅允许选择不同的值, UNION ALL 允许重复

## ANY|ALL

>用于检查 WHERE 或 HAVING 子句中使用的子查询条件的运算符

- ANY 如果任何子查询值满足条件，则返回 true。
- ALL 如果所有子查询值都满足条件，则返回 true。

```sql
SELECT columns_names FROM table1 WHERE column_name operator (ANY|ALL) (SELECT column_name FROMtable_name WHERE condition);
```

## GROUP BY

>通常与聚合函数（COUNT，MAX，MIN，SUM，AVG）一起使用，用于将结果集分组为一列或多列

```sql
SELECT column_name1, COUNT(column_name2) FROM table_name WHERE condition GROUP BY column_name1 ORDER BY COUNT(column_name2) DESC;
```

## HAVING

>HAVING 子句指定 SELECT 语句应仅返回聚合值满足指定条件的行

?>它被添加到 SQL 语言中，因为WHERE关键字不能与聚合函数一起使用。

```sql
SELECT COUNT(column_name1), column_name2 FROM table GROUP BY column_name2 HAVINGCOUNT(column_name1) > 5;
```
