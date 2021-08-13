---
description: 'Saiba mais sobre: JET_INSTANCE. Método Equals (Object)'
title: JET_INSTANCE. Método Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 490e5763aa1754387db67fcd52b6b2a5383affa5d061905b26bafb52acd35716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765660"
---
# <a name="jet_instanceequals-method-object"></a>JET_INSTANCE. Método Equals (Object)

Retorna um valor que indica se essa instância é igual a outra instância.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Parâmetros

  - obj  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Um objeto a ser comparado com essa instância.

#### <a name="return-value"></a>Valor retornado

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias forem iguais.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_INSTANCE](./jet-instance-structure.md)

[Membros do JET_INSTANCE](./jet-instance-members.md)

[Sobrecarga de Equals](./jet-instance.equals-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
