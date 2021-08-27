---
description: 'Saiba mais sobre: estrutura JET_OBJECTLIST dados'
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
ms.openlocfilehash: 21a3ea030421406a5bc571bb5cc1887f77b4710d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983119"
---
# <a name="jet_objectlist-structure"></a>Estrutura JET_OBJECTLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_objectlist-structure"></a>Estrutura JET_OBJECTLIST

A **JET_OBJECTLIST** de dados percorre uma tabela temporária que foi criada com [JetGetObjectInfo](./jetgetobjectinfo-function.md). Cada linha na tabela temporária descreve um objeto no banco de dados.

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

**Cbstruct**

O tamanho da estrutura, em bytes. A chamada à API atualizará esse campo, portanto, o chamador deve garantir que esse valor corresponde a sizeof( JET_INDEXLIST ).

**Tableid**

O identificador de tabela da tabela temporária que foi criada. O chamador deve conter código que fechará a tabela.

**cRecord**

O número de registros na tabela temporária que foi criada.

**columnidcontainername**

O identificador de coluna do nome do tipo de contêiner.

Os únicos contêineres com suporte no momento são tabelas. Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

O identificador de coluna do nome do objeto.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

O identificador de coluna do tipo do objeto . Os únicos contêineres com suporte no momento são tabelas, portanto, esse campo será JET_objtypTable.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsoleto. Não use.

**columniddtUpdate**

Obsoleto. Não use.

**columnidgrbit**

O identificador de coluna dos **grbits** aplicáveis ao objeto . Para ver uma lista de **grbits aplicáveis,** [consulte JET_TABLECREATE](./jet-tablecreate-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

O identificador de coluna dos sinalizadores aplicáveis ao objeto . Para ver uma lista de sinalizadores aplicáveis, [consulte JET_OBJECTINFO](./jet-objectinfo-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

O identificador de coluna do número de registros que estão presentes na tabela nomeada em **columnidobjectname**.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

O identificador de coluna do número de páginas que o objeto usa.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Comentários

Cada linha na tabela temporária corresponde a um objeto no banco de dados.

Quando a tabela temporária é criada com o parâmetro *InfoLevel* na função [JetGetObjectInfo](./jetgetobjectinfo-function.md) definida como JET_ObjInfoListNoStats, as colunas identificadas por **columnidcRecord** e **columnidcPage** não conterão informações significativas.

Atualmente, somente as informações sobre tabelas estarão na tabela temporária.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



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
