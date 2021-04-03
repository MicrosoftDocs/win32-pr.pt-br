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
ms.openlocfilehash: f08dc8d80a9d62a0cb837e4d4d1fd5e60e025c5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922848"
---
# <a name="jet_indexidinequality-operator"></a>JET_INDEXID. Operador de desigualdade

Determina se duas instâncias especificadas do JET_INDEXID não são iguais.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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

  - lhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias não forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_INDEXID](./jet-indexid-structure2.md)

[Membros do JET_INDEXID](./jet-indexid-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
