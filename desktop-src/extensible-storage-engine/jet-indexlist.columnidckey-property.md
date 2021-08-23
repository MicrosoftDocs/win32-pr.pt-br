---
description: 'Saiba mais sobre a propriedade: JET_INDEXLIST. columnidcKey'
title: Propriedade JET_INDEXLIST. columnidcKey
TOCTitle: 'columnidcKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidckey(v=EXCHG.10)
ms:contentKeyID: 55103598
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4d13e55184beaa67fdecff2c0b2904dba1cc6832338f7bc73cdd0b0790a426e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980187"
---
# <a name="jet_indexlistcolumnidckey-property"></a>Propriedade JET_INDEXLIST. columnidcKey

Obtém o columnid da coluna na tabela temporária que armazena o número de chaves exclusivas no índice. Esse valor não é atual e só é atualizado por "API. JetComputeStats". A coluna é do tipo [Long](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcKey As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcKey
```

``` csharp
public JET_COLUMNID columnidcKey { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Membros do JET_INDEXLIST](./jet-indexlist-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
