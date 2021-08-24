---
description: 'Saiba mais sobre: estrutura de JET_OBJECTLIST'
title: Estrutura JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b746a16677fd9d064eef62735f7529d3652acea95fa95e1beefe4a052aec1c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107725"
---
# <a name="jet_objectlist-structure"></a>Estrutura JET_OBJECTLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_objectlist-structure"></a>Estrutura JET_OBJECTLIST

A estrutura de **JET_OBJECTLIST** atravessa uma tabela temporária que foi criada com [JetGetObjectInfo](./jetgetobjectinfo-function.md). Cada linha na tabela temporária descreve um objeto no banco de dados.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura, em bytes. A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_INDEXLIST).

**TableID**

O identificador de tabela da tabela temporária que foi criada. O chamador deve conter o código que fechará a tabela.

**cRecord**

O número de registros na tabela temporária que foi criado.

**columnidcontainername**

O identificador de coluna do nome do tipo de contêiner.

Os únicos contêineres com suporte atualmente são tabelas. Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

O identificador de coluna do nome do objeto.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

O identificador de coluna do tipo do objeto. Os únicos contêineres com suporte atualmente são tabelas, portanto, esse campo será JET_objtypTable.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsoleto. Não use.

**columniddtUpdate**

Obsoleto. Não use.

**columnidgrbit**

O identificador de coluna do **grbits** que é aplicável ao objeto. Para obter uma lista de **grbits** aplicáveis, consulte [JET_TABLECREATE](./jet-tablecreate-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

O identificador de coluna dos sinalizadores que são aplicáveis ao objeto. Para obter uma lista de sinalizadores aplicáveis, consulte [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

O identificador de coluna do número de registros que estão presentes na tabela nomeada em **columnidobjectname**.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

O identificador de coluna do número de páginas usado pelo objeto.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Comentários

Cada linha na tabela temporária corresponde a um objeto no banco de dados.

Quando a tabela temporária é criada com o parâmetro *InfoLevel* na função [JetGetObjectInfo](./jetgetobjectinfo-function.md) definida como JET_ObjInfoListNoStats, as colunas identificadas por **columnidcRecord** e **columnidcPage** não conterá informações significativas.

Atualmente, somente as informações sobre tabelas estarão na tabela temporária.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
