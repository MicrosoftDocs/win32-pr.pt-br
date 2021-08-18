---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotTruncateLog'
title: Método VistaApi. JetOSSnapshotTruncateLog (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d216a79934485ed2ea447bd31e93de575e068aa2f548315c2665759aec7a7708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106804"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a>Método VistaApi. JetOSSnapshotTruncateLog

Habilita o truncamento de log para todas as instâncias que fazem parte da sessão de instantâneo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instantâneo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    O identificador do instantâneo.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Opções para esta chamada.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) . Caso contrário, a sessão de instantâneo termina após a chamada para [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaApi](./vistaapi-class.md)

[Membros do VistaApi](./vistaapi-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
