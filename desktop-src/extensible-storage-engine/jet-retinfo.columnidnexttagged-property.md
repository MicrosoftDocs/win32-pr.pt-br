---
description: 'Saiba mais sobre a propriedade: JET_RETINFO. columnidNextTagged'
title: Propriedade JET_RETINFO. columnidNextTagged
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64114b1e998d47a2610e414304e7837ecbb17fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814102"
---
# <a name="jet_retinfocolumnidnexttagged-property"></a>Propriedade JET_RETINFO. columnidNextTagged

Obtém o columnid da coluna com valor marcado, com vários valores ou esparsos, quando todas as colunas marcadas são recuperadas passando 0 como columnid para JetRetrieveColumn.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RETINFO
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_RETINFO](./jet-retinfo-class.md)

[Membros do JET_RETINFO](./jet-retinfo-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
