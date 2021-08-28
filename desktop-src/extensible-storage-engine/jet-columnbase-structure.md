---
description: 'Saiba mais sobre: estrutura de JET_COLUMNBASE'
title: Estrutura JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: eb9ac3377e97079794a8d4c81d4f8be59587870c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468643"
---
# <a name="jet_columnbase-structure"></a>Estrutura JET_COLUMNBASE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columnbase-structure"></a>Estrutura JET_COLUMNBASE

A estrutura de **JET_COLUMNBASE** descreve os parâmetros de uma coluna base. As funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usam a estrutura **JET_COLUMNBASE** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho dessa estrutura, em bytes. Defina **cbStruct** como sizeof (JET_COLUMNBASE).

**columnid**

Reservado. Defina **columnid** como 0 (zero).

**coltyp**

O tipo da coluna (por exemplo, texto, binário ou numérico). Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. Defina como 0 (zero).

**langid**

Reservado. Defina como 0 (zero).

**cp**

A página de código da coluna. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de zero significa que o padrão será usado (Inglês, 1252). Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.

**wFiller**

Reservado. Defina como 0 (zero).

**cbMax**

O comprimento máximo, em bytes, de uma coluna de comprimento variável ou o comprimento real, em bytes, de uma coluna de comprimento fixo.

**grbit**

Opções para a coluna, incluindo zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>A coluna é fixada e ocupa a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que ela contém. JET_bitColumnFixed não pode ser combinada com JET_bitColumnTagged e não pode ser usada quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLongText</strong> ou <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>A coluna será marcada e ocupará espaço no banco de dados somente se ele contiver dado. JET_bitColumnTagged não pode ser combinado com JET_bitColumnFixed, JET_bitColumnVersion ou JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>A coluna não deve ser definida como um valor <strong>nulo</strong> .</p><p>JET_bitColumnNotNULL não pode ser combinado com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>A coluna é uma coluna de versão que especifica a versão da linha. O valor dessa coluna começa em zero e é incrementado automaticamente para cada atualização da linha.</p><p>JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLong</strong> e não pode ser combinado com JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged ou JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>A coluna é incrementada automaticamente. O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela. No entanto, os números podem não ser sequenciais. Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna incrementada automaticamente poderá conter os valores {1, 2, 6, 7, 8}.</p><p>JET_bitColumnAutoincrement pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong> e não pode ser combinado com JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault ou JET_bitColumnVersion.</p><p><strong>Windows 2000:</strong> JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Válido somente para chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>. JET_bitColumnUpdatable não pode ser combinado com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Válido somente em chamadas para <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>A coluna pode ter valores múltiplos. Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com valores múltiplos são identificados por um número no membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, elas podem não ser colunas de comprimento fixo ou de comprimento variável.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Especifica que uma coluna é uma coluna de atualização de caução que pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e terá consistência transacional.</p><ul><li><p>Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</p></li></ul><ul><li><p>Para uma coluna de atualização de caução, o membro <strong>coltyp</strong> deve ser definido como <strong>JET_coltypLong.</strong></p></li></ul><ul><li><p>Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate não pode ser combinado com JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>A coluna é criada sem um número de versão. Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão. JET_bitColumnUnversioned é usado somente com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Ele não pode ser usado em uma transação.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p><p>JET_bitColumnMaybeNull não pode ser combinado com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Não use. Em vez disso, use JET_bitColumnDeleteOnZero.</p><p>A coluna pode ser finalizada. Uma coluna que pode ser finalizada é uma coluna de atualização de caução que faz com que a linha seja excluída quando a coluna chega a zero. Versões futuras podem invocar uma função de retorno de chamada em vez disso (consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução. JET_bitColumnFinalize não pode ser combinado com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>O valor padrão de uma coluna será fornecido por uma função de retorno de chamada. Consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. Se JET_bitColumnUserDefinedDefault for especificado, o <strong>pvDefault</strong> deverá apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deverá ser definido como sizeof (JET_USERDEFINEDDEFAULT).</p><p>JET_bitColumnUserDefinedDefault não pode ser combinado com JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído. Um uso comum para colunas Delete-on-zero é como campos de contagem de referência. Quando o número de referências cair para zero, o registro será excluído. Uma coluna delete-on-zero deve ser uma coluna de atualização de escrow.</p><p>JET_bitColumnDeleteOnZero substitui JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero pode ser combinado com JET_bitColumnFinalize ou JET_bitColumnUserDefinedDefault e não pode ser usado com colunas padrão definidas pelo usuário.</p> | 



**szBaseTableName**

A tabela da qual a tabela atual herda sua DDL.

**szBaseColumnName**

O nome da coluna na tabela de modelo.

### <a name="remarks"></a>Comentários

**JET_COLUMNBASE** contém grande parte das mesmas informações que [JET_COLUMNDEF](./jet-columndef-structure.md), mas adiciona campos de cadeia de caracteres para descrever a tabela base (se uma DDL hierárquica foi usada).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_COLUMNBASE_W</strong> (Unicode) <strong>e JET_COLUMNBASE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
