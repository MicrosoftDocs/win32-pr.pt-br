---
description: 'Saiba mais sobre: estrutura JET_INDEXRANGE dados'
title: estrutura JET_INDEXRANGE de dados
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
ms.openlocfilehash: 48e9da5822f69d4460a1699252112899a990188d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470872"
---
# <a name="jet_indexrange-structure"></a>estrutura JET_INDEXRANGE de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexrange-structure"></a>estrutura JET_INDEXRANGE de dados

A **JET_INDEXRANGE** de dados identifica um intervalo de índice quando é usado com a [função JetIntersectIndexes.](./jetintersectindexes-function.md)

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho, em bytes, do **JET_INDEXRANGE**.

**Tableid**

Um cursor que anteriormente tinha um intervalo de índice definido com [JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Um bitmask composto exatamente por um dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>Especifica que o intervalo de índice deve ser tratado normalmente.</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>Reservado para uso futuro. Não use.</p> | 



### <a name="remarks"></a>Comentários

Cada **JET_INDEXRANGE** estrutura passada para [JetIntersectIndexes](./jetintersectindexes-function.md) representa um intervalo de índices, que será interseccionada pela chamada à API. O cursor que é dado **em JET_INDEXRANGE** deve ter um intervalo de índice válido definido nele já, com uma chamada bem-sucedida para [JetSetIndexRange](./jetsetindexrange-function.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
