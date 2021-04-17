---
description: 'Saiba mais sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100881
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
ms.openlocfilehash: e345db028422733d37d50f51cfd0c940823f9f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763494"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--setcolumngrbit"></a>Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)

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
    data As Byte(), _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    SetColumnGrbit grbit
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
    Escreva \[\]  
    
    Os dados a serem definidos.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)  
    
    Opções SetColumn.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de SetColumn](./api.setcolumn-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
