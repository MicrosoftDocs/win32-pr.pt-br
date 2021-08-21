---
description: 'Saiba mais sobre: JET_INDEXID. Operador de desigualdade'
title: JET_INDEXID. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510422
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57be54abcf6d58da331334dc5af8c7ea8902da35c33b8d4897990b733a8067a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038974"
---
# <a name="jet_indexidinequality-operator"></a>JET_INDEXID. Operador de desigualdade

Determina se duas instâncias especificadas do JET_INDEXID são iguais.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias não são iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INDEXID estrutura](./jet-indexid-structure2.md)

[JET_INDEXID membros](./jet-indexid-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
