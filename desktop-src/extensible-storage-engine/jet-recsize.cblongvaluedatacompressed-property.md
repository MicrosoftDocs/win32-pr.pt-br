---
description: 'Saiba mais sobre: JET_RECSIZE.cbLongValueDataCompressed'
title: JET_RECSIZE.cbLongValueDataCompressed (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e7ea71f705c14ef7c62244fde691e1a1174216fd07fa06b49e97d2fd124c592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038844"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a>JET_RECSIZE.cbLongValueDataCompressed

Obtém o tamanho compactado dos dados do usuário na árvore de valor longo. Isso será o mesmo que [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) se nenhum valor longo separado for compactado.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_RECSIZE estrutura](./jet-recsize-structure2.md)

[JET_RECSIZE membros](./jet-recsize-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
