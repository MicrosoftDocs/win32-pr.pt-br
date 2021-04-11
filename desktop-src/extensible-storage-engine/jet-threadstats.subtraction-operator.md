---
description: 'Saiba mais sobre: JET_THREADSTATS. Operador de subtração'
title: JET_THREADSTATS. Operador de subtração (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164264"
---
# <a name="jet_threadstatssubtraction-operator"></a>JET_THREADSTATS. Operador de subtração

Calcule a diferença em estatísticas entre duas estruturas de JET_THREADSTATS.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parâmetros

  - t1  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    O primeiro JET_THREADSTATS.

<!-- end list -->

  - T2  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    A segunda JET_THREADSTATS.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Uma JET_THREADSTATS que contém a diferença em estatísticas entre T1 e T2.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membros do JET_THREADSTATS](./jet-threadstats-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
