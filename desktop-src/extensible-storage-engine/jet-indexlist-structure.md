---
description: 'Saiba mais sobre: estrutura de JET_INDEXLIST'
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
ms.openlocfilehash: e21353fb780ed7346c1ff82cbc5057469da25a4b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987479"
---
# <a name="jet_indexlist-structure"></a>Estrutura JET_INDEXLIST


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_indexlist-structure"></a>Estrutura JET_INDEXLIST

A estrutura de **JET_INDEXLIST** contém as informações necessárias para atravessar uma tabela temporária que é criada pelas funções [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) . Cada linha na tabela temporária descreve uma coluna de um índice.

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

**cbStruct**

O tamanho da estrutura em bytes. A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_INDEXLIST).

**TableID**

O identificador de tabela da tabela temporária que foi criada. É responsabilidade do chamador fechar a tabela.

**cRecord**

O número de registros na tabela temporária que foi criado.

**columnidindexname**

O identificador de coluna do nome do índice.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

O identificador de coluna do *grbits* usado no índice. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter uma lista de bits válidos.

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

O identificador de coluna do número de colunas no índice. Para obter mais informações, consulte a seção comentários deste tópico.

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Especifica que 15 colunas são permitidas.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Especifica que 14 colunas são permitidas.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Especifica que são permitidas 9 colunas.</p> | 



**columnidcolumnid**

O identificador de coluna da coluna que é indexada. Para obter mais informações, consulte a seção comentários deste tópico. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

O identificador de coluna do coltyp da coluna que é indexada. Para obter mais informações, consulte a seção comentários deste tópico. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

O identificador de coluna do código de país da coluna que é indexada. O código do país é preterido.

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

O identificador de coluna do identificador de idioma (LCID) sob o qual o índice foi criado. Para obter mais informações, consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

O identificador de coluna da página de código sob a qual o índice foi criado. Para obter mais informações, consulte [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

O identificador de coluna da sequência de agrupamento sob a qual o índice foi criado. A sequência de agrupamento foi preterida.

Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

O identificador de coluna do *grbits* que se aplica à ordem da coluna no índice.

Os dados desta coluna podem ser ordenados como JET_bitKeyAscending ou JET_bitKeyDescending. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md). Por exemplo, um índice definido como "-Coluna1 \\ 0 + Coluna2 \\ 0" terá JET_bitKeyDescending para "Column1" e JET_bitKeyAscending para "Coluna2".

As opções a seguir são válidas para este membro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Um segmento de índice em ordem crescente.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Um segmento de índice em ordem decrescente.</p> | 



**columnidcolumnname**

O identificador de coluna do nome da coluna.

Esta coluna é uma [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

O identificador de coluna dos sinalizadores que são usados para criar o índice. Para obter mais informações, consulte a seção **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Comentários

Cada linha na tabela temporária corresponde a uma coluna em um índice específico.

Por exemplo, o índice "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" tem mais de cinco colunas e ocupará cinco linhas na tabela temporária. Cada uma dessas cinco linhas terá um valor de 5 na coluna identificada pela coluna columnid. Mas cada linha terá um valor diferente para a coluna columnid, variando de 0 a 4.

O número de chaves em um índice específico corresponde ao número de valores exclusivos para os quais um chamador pode buscar e obter uma correspondência exata. O número de entradas é o número de linhas que um índice corresponde. Se um índice tiver uma restrição de exclusividade, o número de chaves será igual ao número de entradas. Por exemplo, se uma tabela contiver as seguintes informações e um índice for criado na coluna chamada "Key", haverá três chaves (100, 200 e 500), mas haverá quatro entradas ("This", "is", "a" e "example").


| <p>Chave</p> | <p>Entrada</p> | 
|------------|--------------|
| <p>100</p> | <p>Esta</p> | 
| <p>100</p> | <p>for</p> | 
| <p>200</p> | <p>um</p> | 
| <p>500</p> | <p>exemplo</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



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
