---
description: 'Saiba mais sobre a propriedade: JET_COLUMNCREATE. CP'
title: Propriedade JET_COLUMNCREATE. CP
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cp(v=EXCHG.10)
ms:contentKeyID: 55103400
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39c47402a70778543f203777b6e2d0d3fc9ac29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782633"
---
# <a name="jet_columncreatecp-property"></a>Propriedade JET_COLUMNCREATE. CP

Obtém ou define a página de código da coluna. Isso só é significativo para colunas do tipo [Text](./jet-coltyp-enumeration.md) e [LONGTEXT](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_COLUMNCREATE](./jet-columncreate-class.md)

[Membros do JET_COLUMNCREATE](./jet-columncreate-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
