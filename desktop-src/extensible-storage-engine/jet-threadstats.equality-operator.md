---
description: 'Saiba mais sobre: JET_THREADSTATS. Operador de igualdade'
title: JET_THREADSTATS. Operador de igualdade (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797664"
---
# <a name="jet_threadstatsequality-operator"></a>JET_THREADSTATS. Operador de igualdade

Determina se duas instâncias especificadas do JET_THREADSTATS são iguais.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - lhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membros do JET_THREADSTATS](./jet-threadstats-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
