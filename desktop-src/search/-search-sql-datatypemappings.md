---
description: A tabela a seguir lista os mapeamentos entre tipos de dados variantes e tipos de dados OLE DB.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Mapeamentos de tipo de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beae5a9ce1fbaafadfae54979d63c97310f57db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090072"
---
# <a name="data-type-mappings"></a>Mapeamentos de tipo de dados

A tabela a seguir lista os mapeamentos entre tipos de dados variantes e tipos de dados OLE DB.




| Tipo de dados Variant | Tipo de dados OLE DB |
|-------------------|------------------|
| BOOL do VT \_          | BOOL de DBTYPE \_     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| ByRef do VT \_         | ByRef de DBTYPE \_    |
| VT \_ Cy            | DBTYPE \_ Cy       |
| Data de VT \_          | data do DBTYPE \_     |
| \_decimal VT       | DBTYPE \_ decimal  |
| VT \_ vazio         | DBTYPE \_ vazio    |
| FILETIME do VT \_      | FILETIME de DBTYPE \_ |
| GUID do VT \_          | \_GUID DbType     |
| VT \_ i1            | DBTYPE \_ i1       |
| \_I2 VT            | DBTYPE \_ i2       |
| \_I4 VT            | DBTYPE \_ i4       |
| VT \_ i8            | DBTYPE \_ i8       |
| VT \_ nulo          | DBTYPE \_ nulo     |
| VT \_ R4            | DBTYPE \_ R4       |
| R8 de VT \_            | DBTYPE \_ UI8      |
| \_vetor VT        | \_vetor DbType   |
| \_WSTR VT          | DBTYPE \_ WSTR     |



 

A tabela a seguir lista os mapeamentos entre tipos de dados XML e OLE DB tipos de dados.



| Tipo de dados Variant | Tipo de dados OLE DB |
|-------------------|------------------|
| Compartimento. BASE64        | BYTES de DBTYPE \_    |
| Compartimento. PRESSÃO           | DBTYPE \_ i8       |
| BOOLEAN           | BOOL de DBTYPE \_     |
| CHAR              | \_Str DbType      |
| DATE              | data do DBTYPE \_     |
| DATETIME          | data do DBTYPE \_     |
| Horário. TZ       | data do DBTYPE \_     |
| CORRIGIDO. 14.4        | DBTYPE \_ R4       |
| FLOAT             | R8 de DBTYPE \_       |
| I1                | DBTYPE \_ i1       |
| I2                | DBTYPE \_ i2       |
| I4                | DBTYPE \_ i4       |
| I8                | DBTYPE \_ i8       |
| INT               | DBTYPE \_ i8       |
| LONG              | DBTYPE \_ i4       |
| NUMBER            | R8 de DBTYPE \_       |
| R4                | DBTYPE \_ R4       |
| R8                | R8 de DBTYPE \_       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | FILETIME de DBTYPE \_ |
| Momento. TZ           | FILETIME de DBTYPE \_ |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | \_GUID DbType     |



 

Você pode converter dados de cadeia de caracteres em outros tipos de dados. Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).

 

 



