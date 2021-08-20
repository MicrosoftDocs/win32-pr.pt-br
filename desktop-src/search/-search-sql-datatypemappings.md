---
description: A tabela a seguir lista os mapeamentos entre tipos de dados variantes e OLE DB tipos de dados.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Mapeamentos de tipo de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e25e909755c87b15526b97488285a0cf688e15dab64073fad603efc190f382b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462590"
---
# <a name="data-type-mappings"></a>Mapeamentos de tipo de dados

A tabela a seguir lista os mapeamentos entre tipos de dados variantes e OLE DB tipos de dados.




| Tipo de dados variant | Tipo de dados OLE DB |
|-------------------|------------------|
| BOOL da VT \_          | DBTYPE \_ BOOL     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| BYREF da VT \_         | DBTYPE \_ BYREF    |
| VT \_ CY            | DBTYPE \_ CY       |
| DATA \_ DA VT          | DBTYPE \_ DATE     |
| DECIMAL \_ da VT       | DBTYPE \_ DECIMAL  |
| VT \_ VAZIO         | DBTYPE \_ VAZIO    |
| FILETIME da VT \_      | DBTYPE \_ FILETIME |
| GUID da VT \_          | DBTYPE \_ GUID     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ I8            | DBTYPE \_ I8       |
| VT \_ NULL          | DBTYPE \_ NULL     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| VETOR de VT \_        | VETOR \_ DBTYPE   |
| VT \_ WSTR          | DBTYPE \_ WSTR     |



 

A tabela a seguir lista os mapeamentos entre tipos de dados XML e OLE DB de dados.



| Tipo de dados variant | Tipo de dados OLE DB |
|-------------------|------------------|
| Bin. BASE64        | DBTYPE \_ BYTES    |
| Bin. Hex           | DBTYPE \_ I8       |
| BOOLEAN           | DBTYPE \_ BOOL     |
| CHAR              | DBTYPE \_ STR      |
| DATE              | DBTYPE \_ DATE     |
| DATETIME          | DBTYPE \_ DATE     |
| Datetime. Tz       | DBTYPE \_ DATE     |
| FIXED.14.4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ I8       |
| INT               | DBTYPE \_ I8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | DBTYPE \_ FILETIME |
| Tempo. Tz           | DBTYPE \_ FILETIME |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | DBTYPE \_ GUID     |



 

Você pode lançar dados de cadeia de caracteres em outros tipos de dados. Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).

 

 



