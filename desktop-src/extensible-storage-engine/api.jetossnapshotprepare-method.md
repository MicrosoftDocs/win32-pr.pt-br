---
description: 'Saiba mais sobre: método API. JetOSSnapshotPrepare'
title: Método API. JetOSSnapshotPrepare
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6e863c13ee46267e18133afc825e9362acfe44d58b64b22bc5105ab8c164bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902956"
---
# <a name="apijetossnapshotprepare-method"></a>Método API. JetOSSnapshotPrepare

Inicia a preparação para uma sessão de instantâneo. Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não emite nenhum IOs de gravação para o disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlada por um gravador de instantâneo).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instantâneo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Retorna a ID da sessão de instantâneo.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)  
    
    Opções de instantâneo.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
