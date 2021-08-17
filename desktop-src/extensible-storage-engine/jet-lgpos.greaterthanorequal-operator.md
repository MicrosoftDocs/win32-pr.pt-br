---
description: 'Saiba mais sobre: JET_LGPOS. Operador GreaterThanOrEqual'
title: JET_LGPOS. Operador GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef9f6835d4c65d08eeb6b3765bd5f2319048986daac439b7b2059b02ecf9735a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109263"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a>JET_LGPOS. Operador GreaterThanOrEqual

Determine se uma posição de log é após ou igual a outra posição de log.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    A primeira posição de log a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    A segunda posição de log a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se lhs vier após ou for igual a rhs.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_LGPOS estrutura](./jet-lgpos-structure2.md)

[JET_LGPOS membros](./jet-lgpos-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
