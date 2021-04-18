---
description: 'Saiba mais sobre: método API. JetGotoPosition'
title: Método API. JetGotoPosition
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5917e729d1a9ae5ae0a3715d6a2a2a81f45f75e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810803"
---
# <a name="apijetgotoposition-method"></a>Método API. JetGotoPosition

Move um cursor para um novo local que é uma fração do caminho por meio do índice atual. Consulte também [JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor a ser posicionado.

<!-- end list -->

  - recpos  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    A posição aproximada para a qual mover.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
