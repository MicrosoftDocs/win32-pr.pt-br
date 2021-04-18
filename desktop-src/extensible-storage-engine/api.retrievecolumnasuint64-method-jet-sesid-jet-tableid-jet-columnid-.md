---
description: 'Saiba mais sobre: método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100864
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ef62c1faa4a7060996d587a92838bdced560350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751162"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid"></a>Método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)

Recupera um valor de coluna UInt64 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.

Esta API não está em conformidade com CLS. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor do qual recuperar a coluna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    O columnid a ser recuperado.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\>  
Os dados recuperados da coluna como um UInt64. NULL se a coluna for nula.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de RetrieveColumnAsUInt64](./api.retrievecolumnasuint64-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
