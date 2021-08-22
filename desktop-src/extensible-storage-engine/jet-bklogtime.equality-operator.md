---
description: 'Saiba mais sobre: JET_BKLOGTIME. Operador de igualdade'
title: JET_BKLOGTIME. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a611dd5207d55fe820e03ac8fef08f0bfe44e89ba190a35eb109d1b3af5ba20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475786"
---
# <a name="jet_bklogtimeequality-operator"></a>JET_BKLOGTIME. Operador de igualdade

Determina se duas instâncias especificadas do JET_BKLOGTIME são iguais.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - lhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Membros do JET_BKLOGTIME](./jet-bklogtime-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
