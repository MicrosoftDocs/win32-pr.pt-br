---
description: 'Saiba mais sobre: JET_INDEXLIST.tableid'
title: propriedade JET_INDEXLIST.tableid
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103670
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a8c1da6b96f0ce842d7287e7f674db07bfd875a83669548de499ddc12de80825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980206"
---
# <a name="jet_indexlisttableid-property"></a>propriedade JET_INDEXLIST.tableid

Obtém tableid da tabela temporária. Isso deve ser fechado quando a tabela não for mais necessária.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INDEXLIST classe](./jet-indexlist-class.md)

[JET_INDEXLIST membros](./jet-indexlist-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
