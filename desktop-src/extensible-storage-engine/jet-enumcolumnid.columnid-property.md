---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMNID. ColumnID'
title: Propriedade JET_ENUMCOLUMNID. ColumnID
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e8aea385dd124e455d26e809c655b25d513a1a7fc843b8b42c8de395c3241c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890856"
---
# <a name="jet_enumcolumnidcolumnid-property"></a>Propriedade JET_ENUMCOLUMNID. ColumnID

Obtém ou define a ID de columnid a ser enumerada.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="remarks"></a>Comentários

Se a ID da coluna for 0 (zero), a enumeração dessa coluna será ignorada e um slot correspondente na matriz de saída de estruturas de JET_ENUMCOLUMN será gerado com um estado de coluna de JET_wrnColumnSkipped.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Membros do JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
