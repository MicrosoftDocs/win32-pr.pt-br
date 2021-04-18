---
description: 'Saiba mais sobre a propriedade: JET_OBJECTLIST. columnidflags'
title: Propriedade JET_OBJECTLIST. columnidflags
TOCTitle: 'columnidflags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidflags(v=EXCHG.10)
ms:contentKeyID: 55103772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidflags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca7e2be41262578b2c4224ebcc97050b8e27bcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760484"
---
# <a name="jet_objectlistcolumnidflags-property"></a>Propriedade JET_OBJECTLIST. columnidflags

Obtém o columnid da coluna na tabela temporária que armazena os sinalizadores de tabela (por exemplo, o sinalizador de tabela do sistema).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Property columnidflags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidflags
```

``` csharp
public JET_COLUMNID columnidflags { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_OBJECTLIST](./jet-objectlist-class.md)

[Membros do JET_OBJECTLIST](./jet-objectlist-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
