---
description: 'Saiba mais sobre: JET_HANDLE. Operador de igualdade'
title: JET_HANDLE. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512271
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bd0c5b037334bef46c44d0da7e0bc47232750ce64e63d922d09c68ced3d4e66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604046"
---
# <a name="jet_handleequality-operator"></a>JET_HANDLE. Operador de igualdade

Determina se duas instâncias especificadas do JET_HANDLE são iguais.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a>Parâmetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    A primeira instância a ser comparada.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    A segunda instância a ser comparada.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias são iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_HANDLE estrutura](./jet-handle-structure.md)

[JET_HANDLE membros](./jet-handle-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
