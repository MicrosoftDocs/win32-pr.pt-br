---
description: 'Saiba mais sobre: Método Api.JetGetRecordPosition'
title: Método Api.JetGetRecordPosition
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
ms.openlocfilehash: 12d4e52ff2b9f2d9935ac7c585b146442f1dc418de5339b1600dc3a89e234e53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042554"
---
# <a name="apijetgetrecordposition-method"></a>Método Api.JetGetRecordPosition

Retorna a posição fracionária do registro atual no índice atual na forma de uma [estrutura JET_RECPOS](./jet-recpos-class.md) dados. Consulte também [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor posicionado no registro.

<!-- end list -->

  - recpos  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    Retorna a posição fracionada aproximada do registro.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
