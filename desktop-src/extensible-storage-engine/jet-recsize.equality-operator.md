---
description: 'Saiba mais sobre: JET_RECSIZE. Operador de igualdade'
title: JET_RECSIZE. Operador de igualdade (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515439
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7b0c34f94d0c59f30283cca3315466ed75ad489719a5d883f7597dd3614fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038744"
---
# <a name="jet_recsizeequality-operator"></a>JET_RECSIZE. Operador de igualdade

Determina se duas instâncias especificadas de JET_RECSIZE são iguais.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias são iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_RECSIZE estrutura](./jet-recsize-structure2.md)

[JET_RECSIZE membros](./jet-recsize-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
