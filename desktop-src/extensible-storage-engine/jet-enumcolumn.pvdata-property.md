---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMN. pvData'
title: Propriedade JET_ENUMCOLUMN. pvData
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df79d838277a849c99ea49af2a8ca12e77cb3667d4750b141f0b9247b46b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254688"
---
# <a name="jet_enumcolumnpvdata-property"></a>Propriedade JET_ENUMCOLUMN. pvData

Obtém o valor que foi enumerado para a coluna. Esse membro só será usado se [Err](./jet-enumcolumn.err-property.md) for igual a [ColumnSingleValue](./jet-wrn-enumeration.md). Isso aponta para a memória alocada com o retorno de chamada de alocador de [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) passado para [JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md). Lembre-se de liberar a memória quando terminar.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Membros do JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
