# niftydatabaseresearch
tricks for navigating unknown data sources

# when you want to find data structures related to a search term
SELECT      c.name  AS 'ColumnName'
            ,t.name AS 'TableName'
FROM        sys.columns c
JOIN        sys.tables  t   ON c.object_id = t.object_id
WHERE       c.name LIKE '%searchterm%'
ORDER BY    TableName
            ,ColumnName; 
 
