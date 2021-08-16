---
description: 'Saiba mais sobre: Método VistaApi.JetOSSnapshotEnd'
title: Método VistaApi.JetOSSnapshotEnd (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8aa385dbba241a631bc7bc29c5ca7905c4a609f6eb2231a984b4c0e9d1db8eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106813"
---
# <a name="vistaapijetossnapshotend-method"></a>Método VistaApi.JetOSSnapshotEnd

Notifica o mecanismo de que a sessão de instantâneo foi concluída.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instantâneo  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    O identificador da sessão de instantâneo.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)  
    
    Opções de fim de instantâneo.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaApi](./vistaapi-class.md)

[Membros do VistaApi](./vistaapi-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
