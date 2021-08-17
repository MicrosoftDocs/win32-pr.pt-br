---
description: 'Saiba mais sobre: método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)'
title: Método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b7ea09ae36160fc83fbee4dc3b7f94222f55125b992039aa15035c1d958c696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117718714"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a>Método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)

Navegar por um índice. O cursor pode ser posicionado no início ou no final do índice e movido para trás e encaminhado por um número especificado de entradas de índice. Consulte também [TryMoveFirst (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada para a chamada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor a ser posicionado.

<!-- end list -->

  - numRows  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)  
    
    Um deslocamento que indica a distância de movimentação do cursor.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. MoveGrbit](./movegrbit-enumeration.md)  
    
    Opções de movimentação.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetMove](./api.jetmove-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
