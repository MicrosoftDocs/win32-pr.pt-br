---
description: 'Saiba mais sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100926
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925d8483a799a23bc6551e6d3d13731c7f1f392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780080"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int64"></a>Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)

Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Long _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As LongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    long data
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor a ser atualizado. Uma atualização deve ser preparada.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    O columnid a ser definido.

<!-- end list -->

  - data  
    Tipo: [System. Int64](/dotnet/api/system.int64)  
    
    Os dados a serem definidos.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de SetColumn](./api.setcolumn-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
