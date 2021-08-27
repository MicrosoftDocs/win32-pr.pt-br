---
description: 'Saiba mais sobre: estrutura JET_INDEXLIST dados'
title: Estrutura JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480042"
---
# <a name="jet_indexlist-structure"></a>Estrutura JET_INDEXLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexlist-structure"></a>Estrutura JET_INDEXLIST

A **JET_INDEXLIST** contém as informações necessárias para percorrer uma tabela temporária criada pelas funções [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md) Cada linha na tabela temporária descreve uma coluna de um índice.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho da estrutura em bytes. A chamada à API atualizará esse campo, portanto, o chamador deve garantir que esse valor corresponde a sizeof( JET_INDEXLIST ).

**Tableid**

O identificador de tabela da tabela temporária que foi criada. É responsabilidade do chamador fechar a tabela.

**cRecord**

O número de registros na tabela temporária que foi criada.

**columnidindexname**

O identificador de coluna do nome do índice.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

O identificador de coluna dos *grbits* usados no índice. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para ver uma lista de bits válidos.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

O identificador de coluna do número de chaves no índice.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

O identificador de coluna do número de entradas no índice.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

O identificador de coluna do número de páginas que o índice usa. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

O identificador de coluna do número total de colunas que o índice abrange.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

O identificador de coluna do número das colunas no índice. Para obter mais informações, consulte a seção Comentários deste tópico.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Especifica que 15 colunas são permitidas.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Especifica que 14 colunas são permitidas.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Especifica que 9 colunas são permitidas.</p> | 



**columnidcolumnid**

O identificador de coluna da coluna que é indexada. Para obter mais informações, consulte a seção Comentários deste tópico. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

O identificador de coluna do coltyp da coluna que é indexada. Para obter mais informações, consulte a seção Comentários deste tópico. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

O identificador de coluna do código do país da coluna indexada. O código do país foi preterido.

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

O identificador de coluna do LCID (identificador de idioma) no qual o índice foi criado. Para obter mais informações, [consulte JET_INDEXCREATE](./jet-indexcreate-structure.md).

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

O identificador de coluna da página de código na qual o índice foi criado. Para obter mais informações, [consulte JET_COLUMNCREATE](./jet-columncreate-structure.md).

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

O identificador de coluna da sequência de collation na qual o índice foi criado. A sequência de collation foi preterida.

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

O identificador de coluna dos *grbits* que se aplicam à ordem da coluna no índice.

Os dados dessa coluna podem ser ordenados como JET_bitKeyAscending ou JET_bitKeyDescending. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md). Por exemplo, um índice definido como "-column1 \\ 0+column2 0" terá JET_bitKeyDescending para \\ "column1" e JET_bitKeyAscending para "column2".

As opções a seguir são válidas para esse membro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Um segmento de índice em ordem crescente.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Um segmento de índice em ordem decrescente.</p> | 



**columnidcolumnname**

O identificador de coluna do nome da coluna.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

O identificador de coluna dos sinalizadores usados para criar o índice. Para obter mais informações, consulte **a seção dwMapFlags** [do JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Comentários

Cada linha na tabela temporária corresponde a uma coluna em um índice específico.

Por exemplo, o índice "+A \\ 0+B \\ 0+C \\ 0+D \\ 0+E 0" é mais de cinco \\ colunas e ocupará cinco linhas na tabela temporária. Cada uma dessas cinco linhas terá um valor de 5 na coluna identificada pela coluna columnid. Mas cada linha terá um valor diferente para a coluna columnid, variando de 0 a 4.

O número de chaves em um índice específico corresponde ao número de valores exclusivos para os quais um chamador pode buscar e obter uma correspondente exata. O número de entradas é o número de linhas que um índice corresponde. Se um índice tiver uma restrição de exclusividade, o número de chaves será igual ao número de entradas. Por exemplo, se uma tabela contiver as informações a seguir e um índice for criado na coluna chamada "key", haverá três chaves (100, 200 e 500), mas haverá quatro entradas ("this", "is", "an" e "example").


| <p>Chave</p> | <p>Entrada</p> | 
|------------|--------------|
| <p>100</p> | <p>Esta</p> | 
| <p>100</p> | <p>for</p> | 
| <p>200</p> | <p>um</p> | 
| <p>500</p> | <p>exemplo</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
