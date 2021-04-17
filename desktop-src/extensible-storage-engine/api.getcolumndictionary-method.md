---
description: 'Saiba mais sobre: método API. GetColumnDictionary'
title: Método API. GetColumnDictionary
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761571"
---
# <a name="apigetcolumndictionary-method"></a>Método API. GetColumnDictionary

Cria um dicionário que mapeia nomes de coluna para suas IDs de coluna.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    O sesid a ser usado.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    A tabela para a qual recuperar as informações.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\>  
Um dicionário que mapeia nomes de coluna para IDs de coluna.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
