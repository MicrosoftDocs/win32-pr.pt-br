---
description: 'Saiba mais sobre: JET_THREADSTATS.cPageRead'
title: JET_THREADSTATS.cPageRead (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cPageRead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageread(v=EXCHG.10)
ms:contentKeyID: 39516296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc2dbc98adb0299cc5d409e4bbb278a9a82ac51d2f19121d8f6d46b0371e6927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832626"
---
# <a name="jet_threadstatscpageread-property"></a>JET_THREADSTATS.cPageRead

Obtém o número total de páginas de banco de dados buscadas do disco pelo mecanismo de banco de dados no thread atual.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cPageRead As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRead
```

``` csharp
public int cPageRead { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_THREADSTATS estrutura](./jet-threadstats-structure2.md)

[JET_THREADSTATS membros](./jet-threadstats-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
