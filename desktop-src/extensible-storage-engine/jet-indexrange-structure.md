---
description: 'Saiba mais sobre: estrutura de JET_INDEXRANGE'
title: Estrutura de JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485594"
---
# <a name="jet_indexrange-structure"></a>Estrutura de JET_INDEXRANGE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexrange-structure"></a>Estrutura de JET_INDEXRANGE

A estrutura de **JET_INDEXRANGE** identifica um intervalo de índice quando ele é usado com a função [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, do **JET_INDEXRANGE**.

**TableID**

Um cursor que anteriormente tinha um intervalo de índice definido com [JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Um bitmask composto de exatamente um dos seguintes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Especifica que o intervalo de índice deve ser tratado normalmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Reservado para uso futuro. Não use.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Comentários

Cada estrutura de **JET_INDEXRANGE** que é passada para [JetIntersectIndexes](./jetintersectindexes-function.md) representa um intervalo de índice, que será interseccionado pela chamada à API. O cursor que é fornecido em **JET_INDEXRANGE** deve ter um conjunto de intervalos de índice válido já, com uma chamada bem-sucedida para [JetSetIndexRange](./jetsetindexrange-function.md).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
