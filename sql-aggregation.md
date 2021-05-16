
# 聚合查询

## COUNT

>返回出现次数

```sql
SELECT COUNT (DISTINCT column_name);
```

## MIN( ) and MAX( )

>返回所选列的最小/最大值

```sql
SELECT MIN (column_names) FROM table_name WHERE condition;
SELECT MAX (column_names) FROM table_name WHERE condition;
```

## AVG( )

>返回数字列的平均值

```sql
SELECT AVG (column_name) FROM table_name WHERE condition;
```

## SUM( )

>返回数值列的总和

```sql
SELECT SUM (column_name) FROM table_name WHERE condition;
```
