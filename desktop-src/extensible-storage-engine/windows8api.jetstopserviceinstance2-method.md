---
description: 'Saiba mais sobre: método Windows8Api. JetStopServiceInstance2'
title: Método Windows8Api. JetStopServiceInstance2 (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010641"
---
# <a name="windows8apijetstopserviceinstance2-method"></a>Método Windows8Api. JetStopServiceInstance2

Prepara uma instância para encerramento. Também pode ser usado para retomar uma pausa anterior.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância (em execução) a ser usada.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. StopServiceGrbit](./stopservicegrbit-enumeration.md)  
    
    As opções para parar ou retomar a instância.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Membros do Windows8Api](./windows8api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
