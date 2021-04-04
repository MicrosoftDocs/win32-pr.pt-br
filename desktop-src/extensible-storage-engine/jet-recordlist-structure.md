---
description: 'Saiba mais sobre: estrutura de JET_RECORDLIST'
title: Estrutura de JET_RECORDLIST
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837066"
---
# <a name="jet_recordlist-structure"></a>Estrutura de JET_RECORDLIST


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>Estrutura de JET_RECORDLIST

A estrutura de **JET_RECORDLIST** localiza os registros que estão na interseção de intervalos de índice especificados quando eles são usados com a função [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de **JET_RECORDLIST** , em bytes.

**TableID**

O identificador de tabela de uma tabela temporária que contém os indicadores para os resultados da consulta. A tabela será fechada automaticamente se a transação atual for revertida com [JetRollback](./jetrollback-function.md); caso contrário, ele deve ser fechado com [JetCloseTable](./jetclosetable-function.md).

**cRecord**

O número de linhas na tabela temporária.

**columnidBookmark**

O identificador de coluna da coluna de indicadores na tabela temporária.

### <a name="remarks"></a>Comentários

A tabela temporária que é identificada por **TableName** tem uma única coluna. Essa única coluna contém indicadores, e cada registro deve caber em um buffer de tamanho JET_cbBookmarkMost bytes.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
[JetRollback](./jetrollback-function.md)
