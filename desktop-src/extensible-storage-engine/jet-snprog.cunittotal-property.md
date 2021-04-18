---
description: 'Saiba mais sobre a propriedade: JET_SNPROG. cunitTotal'
title: Propriedade JET_SNPROG. cunitTotal
TOCTitle: 'cunitTotal property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snprog.cunittotal(v=EXCHG.10)
ms:contentKeyID: 55103955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.set_cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.get_cunitTotal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983e07dd56dd75b374a6e869f5614662ad92d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771782"
---
# <a name="jet_snprogcunittotal-property"></a>Propriedade JET_SNPROG. cunitTotal

Obtém o número de unidades de trabalho que precisam ser concluídas. Esse valor sempre será maior ou igual a cunitDone.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cunitTotal As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_SNPROG
Dim value As Integer

value = instance.cunitTotal
```

``` csharp
public int cunitTotal { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_SNPROG](./jet-snprog-class.md)

[Membros do JET_SNPROG](./jet-snprog-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
