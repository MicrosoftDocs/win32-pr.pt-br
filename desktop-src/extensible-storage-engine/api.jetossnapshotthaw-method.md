---
description: 'Saiba mais sobre: método API. JetOSSnapshotThaw'
title: Método API. JetOSSnapshotThaw
TOCTitle: 'JetOSSnapshotThaw method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.SnapshotThawGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotthaw(v=EXCHG.10)
ms:contentKeyID: 55100780
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3fe0bc04586dddade7a9723720bbd3c994c516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837163"
---
# <a name="apijetossnapshotthaw-method"></a>Método API. JetOSSnapshotThaw

Notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento e um instantâneo bem-sucedido.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotThaw ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotThawGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotThawGrbitApi.JetOSSnapshotThaw(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotThaw(
    JET_OSSNAPID snapshot,
    SnapshotThawGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instantâneo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    A ID do instantâneo.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)  
    
    Descongelar opções.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
