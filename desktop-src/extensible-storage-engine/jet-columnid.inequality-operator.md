---
description: 'Saiba mais sobre: JET_COLUMNID. Operador de desigualdade'
title: JET_COLUMNID. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516136
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 409ca5791e57a74133b1c1e7ef6d05166bf2ab2cd8d901bd3d90b12078bbfbc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668096"
---
# <a name="jet_columnidinequality-operator"></a>JET_COLUMNID. Operador de desigualdade

Determina se duas instâncias especificadas do JET_COLUMNID são iguais.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias não são iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_COLUMNID estrutura](./jet-columnid-structure.md)

[JET_COLUMNID membros](./jet-columnid-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
