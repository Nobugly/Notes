# SQLite学习笔记

## SQLite基本数据类型
> * INTEGER
> * FLOAT
> * DOUBLE
> * CHAR
> * VARCHAR

## SQLite用法回顾
**创建表：**
```SQL
CREATE TABLE 表名(字段名 数据类型 约束类型,字段名 数据类型 约束类型,......)
CREATE TABLE person(_id INTEGER PRIMARY KEY,name VARCHAR(16) NOT NULL,age INTEGER)
```
**删除表：**
```SQL
DROP TABLE 表名
DROP TABLE person
```

**Insert语句：**
```SQL
INSERT INTO 表名(字段名,字段名) VALUES(值1,值2)
INSERT INTO person(name,age) VALUES('Richyeoh',18)
INSERT INTO person VALUES(2,'杨明明',19)
```

**Delete语句：**
```SQL
DELETE FROM 表名 WHERE 条件语句
DELETE FROM person WHERE name = 'Richyeoh'
DELETE FROM person WHERE age = 18
```
**注意：如果没有加`WHERE`会替换整个表**

**Update语句：**
```SQL
UPDATE 表名 SET 字段名 = 新值 WHERE 条件语句
UPDATE person SET name = '泽被苍生' WHERE name = 'Richyeoh'
```

**Query语句：**
```SQL
完整的查询语句
SELECT 字段名 FROM 表名 WHERE 条件语句 GROUP BY 分组字段名 HAVING 筛选条件 ORDER BY 排序
常用的查询语句
SELECT 字段名 FROM 表名 WHERE 条件语句
SELECT * FROM person WHERE name = 'Richyeoh'
SELECT name,age FROM person
```
