# 查看所有表和表注释
    select
    *
    from
    INFORMATION_SCHEMA.Tables
    where
    table_schema = ‘数据库名称’
    [TABLE_NAME=表名,TABLE_COMMENT=表注释]

# 查看所有字段和字段注释
    select
    COLUMN_NAME，
    COLUMN_COMMENT
    from
    INFORMATION_SCHEMA.Columns
    where
    table_name = ‘表名’
    and table_schema=‘数据库名’
    【COLUMN_NAME=列名，COLUMN_COMMENT=列注释】
    
# 查询 MySQL 某个库的所有表名和表数据总数

    SELECT table_name,table_rows 
    FROM information_schema.tables  
    WHERE table_schema='库名称' ORDER BY table_rows DESC; 
    
# 查询某个库的某个表字段以及注释

    SELECT
        COLUMN_NAME 字段名,
        column_comment 字段说明,
        column_type 字段类型,
        column_key 约束 
    FROM
        information_schema.COLUMNS 
    WHERE
        table_schema = 'parking' 
        AND table_name = 'road_info';
