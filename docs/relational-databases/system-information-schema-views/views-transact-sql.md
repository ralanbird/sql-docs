---
title: VIEWS (Transact-SQL)
description: "VIEWS (Transact-SQL)"
ms.prod: sql
ms.prod_service: "database-engine, sql-database, synapse-analytics, pdw"
ms.reviewer: ""
ms.technology: system-objects
ms.topic: "reference"
f1_keywords: 
  - "VIEWS_TSQL"
  - "VIEWS"
dev_langs: 
  - "TSQL"
helpviewer_keywords: 
  - "VIEWS view"
  - "INFORMATION_SCHEMA.VIEWS view"
author: markingmyname
ms.author: maghan
ms.custom: ""
ms.date: "03/15/2017"
monikerRange: ">=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current"
---
# VIEWS (Transact-SQL)

[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

Returns one row for views that can be accessed by the current user in the current database.  
  
To retrieve information from these views, specify the fully qualified name of **INFORMATION_SCHEMA.**_view_name_.  
  
|Column name|Data type|Description|  
|-----------------|---------------|-----------------|  
|**TABLE_CATALOG**|**nvarchar(**128**)**|View qualifier.|  
|**TABLE_SCHEMA**|**nvarchar(**128**)**|Name of schema that contains the view.<br /><br /> **&#42;&#42; Important &#42;&#42;**  only reliable way to find the schema of a object is to query the sys.objects catalog view.|  
|**TABLE_NAME**|**nvarchar(**128**)**|View name.|  
|**VIEW_DEFINITION**|**nvarchar(**4000**)**|If the length of definition is larger than **nvarchar(**4000**)**, this column is NULL. Otherwise, this column is the view definition text.|  
|**CHECK_OPTION**|**varchar(**7**)**|Type of WITH CHECK OPTION. Is CASCADE if the original view was created by using the WITH CHECK OPTION. Otherwise, NONE is returned.|  
|**IS_UPDATABLE**|**varchar(**2**)**|Specifies whether the view is updatable. Always returns NO.|  
  
## See Also  
 [System Views &#40;Transact-SQL&#41;](../../t-sql/language-reference.md)   
 [Information Schema Views &#40;Transact-SQL&#41;](~/relational-databases/system-information-schema-views/system-information-schema-views-transact-sql.md)   
 [sys.sql_modules &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-sql-modules-transact-sql.md)   
 [sys.views &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-views-transact-sql.md)  
  
