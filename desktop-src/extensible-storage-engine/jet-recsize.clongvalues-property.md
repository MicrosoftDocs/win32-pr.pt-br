---
description: 'Saiba mais sobre: JET_RECSIZE.cLongValues'
title: JET_RECSIZE.cLongValues (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cLongValues property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.clongvalues(v=EXCHG.10)
ms:contentKeyID: 39515366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd50ba8e934540572f7af9422c7c02e595b9ddf21095460dff82839004584804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730086"
---
# <a name="jet_recsizeclongvalues-property"></a>JET_RECSIZE.cLongValues

Obtém o número total de valores longos armazenados na árvore de valor longo para esse registro. Isso não inclui valores longos intrínsecos.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cLongValues As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cLongValues
```

``` csharp
public long cLongValues { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_RECSIZE estrutura](./jet-recsize-structure2.md)

[JET_RECSIZE membros](./jet-recsize-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
