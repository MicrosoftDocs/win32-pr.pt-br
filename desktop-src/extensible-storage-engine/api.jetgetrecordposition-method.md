---
description: 'Saiba mais sobre: método API. JetGetRecordPosition'
title: Método API. JetGetRecordPosition
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501507"
---
# <a name="apijetgetrecordposition-method"></a>Método API. JetGetRecordPosition

Retorna a posição fracionária do registro atual no índice atual na forma de uma estrutura de [JET_RECPOS](./jet-recpos-class.md) . Consulte também [JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor posicionado no registro.

<!-- end list -->

  - recpos  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    Retorna a posição fracionária aproximada do registro.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
