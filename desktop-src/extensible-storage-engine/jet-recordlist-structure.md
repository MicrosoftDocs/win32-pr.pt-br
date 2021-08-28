---
description: 'Saiba mais sobre: estrutura JET_RECORDLIST dados'
title: estrutura JET_RECORDLIST de JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 983a0d6a73d4a3bb5e44095f46cc52d537ce15f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465093"
---
# <a name="jet_recordlist-structure"></a>estrutura JET_RECORDLIST de JET_RECORDLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_recordlist-structure"></a>estrutura JET_RECORDLIST de JET_RECORDLIST

A **JET_RECORDLIST** localiza registros que estão na interseção de intervalos de índice especificados quando são usados com a [função JetIntersectIndexes.](./jetintersectindexes-function.md)

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho da estrutura **JET_RECORDLIST,** em bytes.

**Tableid**

O identificador de tabela de uma tabela temporária que contém os indicadores para os resultados da consulta. A tabela será fechada automaticamente se a transação atual for re rollback com [JetRollback](./jetrollback-function.md); caso contrário, ele deverá ser fechado com [JetCloseTable.](./jetclosetable-function.md)

**cRecord**

O número de linhas na tabela temporária.

**columnidBookmark**

O identificador de coluna da coluna de indicador na tabela temporária.

### <a name="remarks"></a>Comentários

A tabela temporária identificada por **tableid** tem uma única coluna. Essa única coluna contém indicadores e cada registro deve caber em um buffer de tamanho JET_cbBookmarkMost bytes.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
