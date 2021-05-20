# 查看所有表和表注释
select
*
from
INFORMATION_SCHEMA.Tables
where
table_schema = ‘数据库名称’
[TABLE_NAME=表名,TABLE_COMMENT=表注释]

查看所有字段和字段注释
select
COLUMN_NAME，
COLUMN_COMMENT
from
INFORMATION_SCHEMA.Columns
where
table_name = ‘表名’
and table_schema=‘数据库名’
【COLUMN_NAME=列名，COLUMN_COMMENT=列注释】
