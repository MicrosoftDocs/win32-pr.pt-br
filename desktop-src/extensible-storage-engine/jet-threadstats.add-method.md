---
description: 'Saiba mais sobre: JET_THREADSTATS. Adicionar método'
title: JET_THREADSTATS. Método Add (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d22427056b126c2fcb49f7e395c4a43161eaee70c9d9ed8b9ac7020be88504fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728906"
---
# <a name="jet_threadstatsadd-method"></a>JET_THREADSTATS. Adicionar método

Adicione as estatísticas em duas estruturas de JET_THREADSTATS.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parâmetros

  - t1  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    O primeiro JET_THREADSTATS.

<!-- end list -->

  - T2  
    Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    A segunda JET_THREADSTATS.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Uma JET_THREADSTATS que contém o resultado da adição das estatísticas em T1 e T2.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membros do JET_THREADSTATS](./jet-threadstats-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
