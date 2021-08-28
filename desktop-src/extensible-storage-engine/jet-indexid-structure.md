---
description: 'Saiba mais sobre: estrutura de JET_INDEXID'
title: Estrutura de JET_INDEXID
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
ms.openlocfilehash: 61e51e85fe990cfeee8a5c1ee048a77179d49766
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475952"
---
# <a name="jet_indexid-structure"></a>Estrutura de JET_INDEXID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexid-structure"></a>Estrutura de JET_INDEXID

A estrutura de **JET_INDEXID** contém uma ID de índice. Uma ID de índice é uma dica usada para acelerar a seleção do índice atual usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Ele é mais útil quando há um número muito grande de índices em uma tabela. A ID do índice pode ser recuperada usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, da ID do índice.

Esse é o tamanho real da ID de índice que é retornada no buffer de saída de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

**rgbIndexId**

Um BLOB opaco de informações que é usado pelo mecanismo para identificar rapidamente um índice em seu cache de esquema.

Não tente interpretar o BLOB de informações. Não é um tamanho definido.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
