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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764718"
---
# <a name="jet_columnbase-structure"></a>Estrutura JET_COLUMNBASE


_**Aplica-se a:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitColumnFixed</p></td>
<td><p>A coluna é fixada e ocupa a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que ela contém. JET_bitColumnFixed não pode ser combinada com JET_bitColumnTagged e não pode ser usada quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLongText</strong> ou <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>A coluna será marcada e ocupará espaço no banco de dados somente se ele contiver dado. JET_bitColumnTagged não pode ser combinado com JET_bitColumnFixed, JET_bitColumnVersion ou JET_bitColumnEscrowUpdate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>A coluna não deve ser definida como um valor <strong>nulo</strong> .</p>
<p>JET_bitColumnNotNULL não pode ser combinado com JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>A coluna é uma coluna de versão que especifica a versão da linha. O valor dessa coluna começa em zero e é incrementado automaticamente para cada atualização da linha.</p>
<p>JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLong</strong> e não pode ser combinado com JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged ou JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>A coluna é incrementada automaticamente. O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela. No entanto, os números podem não ser sequenciais. Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna incrementada automaticamente poderá conter os valores {1, 2, 6, 7, 8}.</p>
<p>JET_bitColumnAutoincrement pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong> e não pode ser combinado com JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault ou JET_bitColumnVersion.</p>
<p><strong>Windows 2000:  </strong> JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Válido somente para chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>. JET_bitColumnUpdatable não pode ser combinado com JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Válido somente em chamadas para <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>A coluna pode ter valores múltiplos. Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com valores múltiplos são identificados por um número no membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, elas podem não ser colunas de comprimento fixo ou de comprimento variável.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Especifica que uma coluna é uma coluna de atualização de caução que pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e terá consistência transacional.</p>
<ul>
<li><p>Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</p></li>
</ul>
<ul>
<li><p>Para uma coluna de atualização de caução, o membro <strong>coltyp</strong> deve ser definido como <strong>JET_coltypLong.</strong></p></li>
</ul>
<ul>
<li><p>Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate não pode ser combinado com JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>A coluna é criada sem um número de versão. Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão. JET_bitColumnUnversioned é usado somente com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Ele não pode ser usado em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Reservado para uso futuro.</p>
<p>JET_bitColumnMaybeNull não pode ser combinado com JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Não use. Em vez disso, use JET_bitColumnDeleteOnZero.</p>
<p>A coluna pode ser finalizada. Uma coluna que pode ser finalizada é uma coluna de atualização de caução que faz com que a linha seja excluída quando a coluna chega a zero. Versões futuras podem invocar uma função de retorno de chamada em vez disso (consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução. JET_bitColumnFinalize não pode ser combinado com JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>O valor padrão de uma coluna será fornecido por uma função de retorno de chamada. Consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. Se JET_bitColumnUserDefinedDefault for especificado, o <strong>pvDefault</strong> deverá apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deverá ser definido como sizeof (JET_USERDEFINEDDEFAULT).</p>
<p>JET_bitColumnUserDefinedDefault não pode ser combinado com JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído. Um uso comum para colunas Delete-on-zero é como campos de contagem de referência. Quando o número de referências cair em zero, o registro será excluído. Uma coluna Delete-on-zero deve ser uma coluna de atualização de caução.</p>
<p>JET_bitColumnDeleteOnZero substitui JET_bitColumnFinalize.</p>
<p>JET_bitColumnDeleteOnZero não pode ser combinada com JET_bitColumnFinalize ou JET_bitColumnUserDefinedDefault e não pode ser usada com colunas padrão definidas pelo usuário.</p></td>
</tr>
</tbody>
</table>


**szBaseTableName**

A tabela da qual a tabela atual herda seu DDL.

**szBaseColumnName**

O nome da coluna na tabela de modelo.

### <a name="remarks"></a>Comentários

**JET_COLUMNBASE** contém grande parte das mesmas informações que [JET_COLUMNDEF](./jet-columndef-structure.md), mas adiciona campos de cadeia de caracteres para descrever a tabela base (se um DDL hierárquico foi usado).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_COLUMNBASE_W</strong> (Unicode) e <strong>JET_COLUMNBASE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
