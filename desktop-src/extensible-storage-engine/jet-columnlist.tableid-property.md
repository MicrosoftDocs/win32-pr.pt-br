---
description: 'Saiba mais sobre: JET_COLUMNLIST.tableid'
title: propriedade JET_COLUMNLIST.tableid
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103528
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36f63afab87196337e0d63d19b309ad269d35df636698011db400d58b4d1d178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486851"
---
# <a name="jet_columnlisttableid-property"></a>propriedade JET_COLUMNLIST.tableid

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
Dim instance As JET_COLUMNLIST
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

[JET_COLUMNLIST classe](./jet-columnlist-class.md)

[JET_COLUMNLIST membros](./jet-columnlist-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
