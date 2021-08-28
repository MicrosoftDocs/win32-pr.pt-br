---
description: 'Saiba mais sobre: estrutura JET_INDEXID dados'
title: estrutura JET_INDEXID de dados
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: 89af1b81b5221ab1cdebc0c91d5340acc62dd330
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983969"
---
# <a name="jet_indexid-structure"></a>estrutura JET_INDEXID de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexid-structure"></a>estrutura JET_INDEXID de dados

A **JET_INDEXID** estrutura contém uma ID de índice. Uma ID de índice é uma dica usada para acelerar a seleção do índice atual usando [JetSetCurrentIndex.](./jetsetcurrentindex-function.md) Ele é mais útil quando há um número muito grande de índices em uma tabela. A ID do índice pode ser recuperada usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho, em bytes, da ID do índice.

Esse é o tamanho real da ID do índice que é retornada no buffer de saída de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

**rgbIndexId**

Um BLOB opaco de informações que é usado pelo mecanismo para identificar rapidamente um índice em seu cache de esquema.

Não tente interpretar o BLOB de informações. Não é um tamanho definido.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
