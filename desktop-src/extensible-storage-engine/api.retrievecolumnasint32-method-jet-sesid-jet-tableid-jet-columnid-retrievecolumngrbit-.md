---
description: 'Saiba mais sobre: método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100859
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e9f963d298610fb36f6b1f9c9ff3a0bfbfa2501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501222"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Recupera um valor de coluna Int32 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
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

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Opções de recuperação.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\>  
Os dados recuperados da coluna como um int. NULL se a coluna for nula.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de RetrieveColumnAsInt32](./api.retrievecolumnasint32-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
