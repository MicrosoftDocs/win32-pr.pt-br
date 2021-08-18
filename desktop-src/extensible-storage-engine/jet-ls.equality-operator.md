---
description: 'Saiba mais sobre: JET_LS. Operador de igualdade'
title: JET_LS. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516469
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equality
- Microsoft.Isam.Esent.Interop.JET_LS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fae9e7d2fc311c272fcda4a2222d1eeb6adb1da75fbfd64bd338f3a65f15581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765012"
---
# <a name="jet_lsequality-operator"></a>JET_LS. Operador de igualdade

Determina se duas instâncias especificadas do JET_LS são iguais.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LS, _
    rhs As JET_LS _
) As Boolean
'Usage
Dim lhs As JET_LS
Dim rhs As JET_LS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LS lhs,
    JET_LS rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - lhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_LS](./jet-ls-structure.md)

[Membros do JET_LS](./jet-ls-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
