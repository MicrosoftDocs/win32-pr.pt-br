---
description: 'Saiba mais sobre: JET_INDEXRANGE.tableid'
title: propriedade JET_INDEXRANGE.tableid
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.tableid(v=EXCHG.10)
ms:contentKeyID: 55103657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.set_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b9352d8d80b2e30ccba5110a1c1f979923cf4f707a863c07bd7adef3ed56c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116025"
---
# <a name="jet_indexrangetableid-property"></a>propriedade JET_INDEXRANGE.tableid

Obtém ou define o cursor que contém o intervalo de índice. O cursor deve ter um intervalo de índice definido com JetSetIndexRange.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Set
'Usage
Dim instance As JET_INDEXRANGE
Dim value As JET_TABLEID

value = instance.tableid

instance.tableid = value
```

``` csharp
public JET_TABLEID tableid { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INDEXRANGE classe](./jet-indexrange-class.md)

[JET_INDEXRANGE membros](./jet-indexrange-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
