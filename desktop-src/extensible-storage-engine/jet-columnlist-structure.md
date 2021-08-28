---
description: 'Saiba mais sobre: estrutura de JET_COLUMNLIST'
title: Estrutura JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 6b7f874c95352ce29954adf46b1682dec89c7a9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471792"
---
# <a name="jet_columnlist-structure"></a>Estrutura JET_COLUMNLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columnlist-structure"></a>Estrutura JET_COLUMNLIST

A estrutura de **JET_COLUMNLIST** contém as informações necessárias para percorrer a tabela temporária que é criada pelas funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) . Cada linha na tabela temporária descreve uma coluna na tabela fornecida na chamada à API. Essa estrutura é usada somente com [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura em bytes. A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_COLUMNLIST).

**TableID**

O identificador de tabela da tabela temporária que foi criada. É responsabilidade do chamador fechar a tabela.

**cRecord**

O número de registros na tabela temporária que foi criado pela chamada à API.

**columnidPresentationOrder**

O identificador de coluna da ordem de apresentação.

A ordem de apresentação é usada para classificar as linhas da tabela temporária. A ordem de apresentação é uma [JET_coltypLong](./jet-coltyp.md)fixa. Se o nível de informação especificado não for um nível compacto, ele também será marcado como JET_bitColumnTTKey.

**columnidcolumnname**

O identificador de coluna do nome da coluna.

Se o nível de informação especificado não foi compactado, ele também será marcado como JET_bitColumnTTKey.

**columnidcolumnid**

O identificador de coluna do identificador de coluna.

O identificador de coluna é um [JET_coltypLong](./jet-coltyp.md)fixo.

**columnidcoltyp**

O identificador de coluna do tipo de coluna.

O tipo de coluna é um [JET_coltypLong](./jet-coltyp.md)fixo.

**columnidCountry**

O identificador de coluna do código do país.

O código do país é um [JET_coltypShort](./jet-coltyp.md)fixo.

**columnidLangid**

O identificador de coluna do identificador de idioma.

O identificador de idioma é um [JET_coltypShort](./jet-coltyp.md)fixo.

**columnidCp**

O identificador de coluna da página de código.

A página de código é uma [JET_coltypShort](./jet-coltyp.md)fixa.

**columnidCollate**

O identificador de coluna da sequência de agrupamento.

A sequência de agrupamento é um [JET_coltypShort](./jet-coltyp.md)fixo.

**columnidcbMax**

O identificador de coluna do campo **cbMax** .

O **cbMax** é um [JET_coltypLong](./jet-coltyp.md)fixo.

**columnidgrbit**

O identificador de coluna do *grbits* da coluna. O campo *grbit* é um [JET_coltypLong](./jet-coltyp.md)fixo. Para obter mais informações sobre esses bits, consulte [JET_COLUMNDEF](./jet-columndef-structure.md).

Estes são os valores possíveis para **columnidgrbit**:

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

O identificador de coluna do valor padrão da coluna.

O valor padrão é um [JET_coltypLongBinary](./jet-coltyp.md).

**columnidBaseTableName**

O identificador de coluna do nome da tabela da qual a tabela foi derivada.

O nome da tabela é um [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

O identificador de coluna do nome da coluna da qual a coluna foi derivada.

O nome da coluna é um [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

O identificador de coluna do nome da definição de coluna.

O nome da definição de coluna é um [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Comentários

Por padrão, a ordem das linhas na tabela temporária é classificada pelo nome da coluna. Ele também pode ser classificado por identificador de coluna. Para obter mais informações sobre como classificar por identificador de coluna, consulte [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

A chamada para [JetGetColumnInfo](./jetgetcolumninfo-function.md) ou [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) pode especificar uma forma compacta de resultados. Se alguma coluna tiver sido herdada de uma tabela de modelo, os resultados do Compact não serão armazenados.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
