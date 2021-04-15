---
description: 'Saiba mais sobre a propriedade: JET_RETRIEVECOLUMN. pvData'
title: Propriedade JET_RETRIEVECOLUMN. pvData
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0809073dd956cf8166463450160d46761eb86fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501946"
---
# <a name="jet_retrievecolumnpvdata-property"></a>Propriedade JET_RETRIEVECOLUMN. pvData

Obtém ou define o buffer que armazenará os dados que serão recuperados da coluna.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Escreva \[\]  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)

[Membros do JET_RETRIEVECOLUMN](./jet-retrievecolumn-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
