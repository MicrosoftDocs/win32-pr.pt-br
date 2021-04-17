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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812384"
---
# <a name="jet_columnlist-structure"></a>Estrutura JET_COLUMNLIST


_**Aplica-se a:** Windows | Windows Server_

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

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
