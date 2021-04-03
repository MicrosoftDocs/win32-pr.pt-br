---
description: 'Saiba mais sobre: JET_INSTANCE. Operador de desigualdade'
title: JET_INSTANCE. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d537b01d3485e7f5e2d1d629c005a228eac92306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091823"
---
# <a name="jet_instanceinequality-operator"></a>JET_INSTANCE. Operador de desigualdade

Determina se duas instâncias especificadas do JET_INSTANCE não são iguais.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - lhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias não forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_INSTANCE](./jet-instance-structure.md)

[Membros do JET_INSTANCE](./jet-instance-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
