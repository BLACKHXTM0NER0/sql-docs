---
title: "sp_fulltext_database (Transact-SQL)"
description: "sp_fulltext_database (Transact-SQL)"
author: markingmyname
ms.author: maghan
ms.date: "03/14/2017"
ms.service: sql
ms.subservice: system-objects
ms.topic: "reference"
f1_keywords:
  - "sp_fulltext_database_TSQL"
  - "sp_fulltext_database"
helpviewer_keywords:
  - "sp_fulltext_database"
dev_langs:
  - "TSQL"
monikerRange: "=azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current"
---
# sp_fulltext_database (Transact-SQL)
[!INCLUDE [SQL Server Azure SQL Database Azure SQL Managed Instance](../../includes/applies-to-version/sql-asdb-asdbmi.md)]

  This is supported for backward compatibility only. **sp_fulltext_database** does not disable the Full-Text Engine for a given database. All user-created databases in [!INCLUDE [ssnoversion-md](../../includes/ssnoversion-md.md)] are always enabled for full-text indexing.  
  
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)] Use [!INCLUDE[ssManStudio](../../includes/ssmanstudio-md.md)] instead.  
  
 :::image type="icon" source="../../includes/media/topic-link-icon.svg" border="false"::: [Transact-SQL syntax conventions](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## Syntax  
  
```  
  
sp_fulltext_database [@action=] 'action'  
```  
  
## Arguments  
`[ @action = ] 'action'`
 Is the action to be performed. **action** is **varchar(20)**, and can be one of these values.  
  
|Value|Description|  
|-----------|-----------------|  
|**enable**|Supported for backward compatibility only. It will rebuild all Fulltext catalogs of the database if the previous state of Fulltext is "disabled".|  
|**disable**|Supported for backward compatibility only.|  
  
## Return Code Values  
 0 (success) or 1 (failure)  
  
## Result Sets  
 None  
  
## Remarks  
 In [!INCLUDE[sql2008-md](../../includes/sql2008-md.md)] and later versions, full-text indexing cannot be turned off. Disabling full-text indexing does not remove rows from **sysfulltextcatalogs** and does not indicate that full-text enabled tables are no longer marked for full-text indexing. All the full-text metadata definitions are still in the system tables.  
  
## Permissions  
 Only members of the **sysadmin** fixed server role and **db_owner** fixed database role can execute **sp_fulltext_database**.  
  
## See Also  
 [DATABASEPROPERTYEX &#40;Transact-SQL&#41;](../../t-sql/functions/databasepropertyex-transact-sql.md)   
 [FULLTEXTSERVICEPROPERTY &#40;Transact-SQL&#41;](../../t-sql/functions/fulltextserviceproperty-transact-sql.md)   
 [System Stored Procedures &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
