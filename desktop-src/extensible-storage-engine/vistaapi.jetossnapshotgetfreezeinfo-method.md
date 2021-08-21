---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotGetFreezeInfo'
title: Método VistaApi. JetOSSnapshotGetFreezeInfo (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e29b4415de0657fadf4832f39ff5b25f39ea52c09f7a8c4f9741b18559db4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070392"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a>Método VistaApi. JetOSSnapshotGetFreezeInfo

Recupera a lista de instâncias e bancos de dados que fazem parte da sessão de instantâneo em um determinado momento.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instantâneo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    O identificador da sessão de instantâneo.

<!-- end list -->

  - numInstances  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Retorna o número de instâncias.

<!-- end list -->

  - instances  
    Escreva \[\]  
    
    Retorna informações sobre as instâncias.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)  
    
    Opções para esta chamada.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaApi](./vistaapi-class.md)

[Membros do VistaApi](./vistaapi-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
