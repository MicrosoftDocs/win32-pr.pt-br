---
description: 'Saiba mais sobre: estrutura de JET_COLUMNCREATE'
title: Estrutura JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: 1b14388f26e21550319b910ac01d9ee0dde4d5890336c91e1fca76bc68cce93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254976"
---
# <a name="jet_columncreate-structure"></a>Estrutura JET_COLUMNCREATE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columncreate-structure"></a>Estrutura JET_COLUMNCREATE

A estrutura de **JET_COLUMNCREATE** descreve uma coluna a ser criada em um banco de dados.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura, em bytes. Este campo deve ser inicializado para **sizeof (JET_COLUMNCREATE)**.

**szColumnName**

O nome da coluna a ser criada. O nome deve atender aos seguintes critérios:

  - Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o nulo de terminação.

<!-- end list -->

  - Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ), ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.

<!-- end list -->

  - Ele não pode começar com um espaço.

<!-- end list -->

  - Ele deve conter pelo menos um caractere que não seja de espaço.

**coltyp**

O tipo da coluna (por exemplo, texto, binário ou numérico). Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).

**cbMax**

O comprimento máximo, em bytes, de uma coluna de comprimento variável. O comprimento da coluna para colunas de comprimento fixo.

**grbit**

Um grupo de bits que contém as opções para essa estrutura e que incluem zero ou mais dos valores a seguir.

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
<td><p>A coluna é fixa. Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que está sendo armazenada na coluna. JET_bitColumnFixed não pode ser usada com JET_bitColumnTagged. Esse bit não pode ser usado com valores longos, como <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>A coluna está marcada. As colunas marcadas não ocupam nenhum espaço no banco de dados se não contiverem. Esse bit não pode ser usado com JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>A coluna nunca deve ser definida como um valor nulo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>A coluna é incrementada automaticamente. O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela. No entanto, o número pode não ser contínuo. Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna AutoIncrement poderá conter os valores {1, 2, 6, 7, 8}.</p>
<p><strong>Windows 2000:</strong> Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong>.</p>
<p><strong>Windows Server 2003 e posterior:</strong> Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Esse bit é válido somente em chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>A coluna pode ter valores múltiplos. Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com valores múltiplos são identificados pelo membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ter colunas de comprimento fixo ou de comprimento variável.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>A coluna é uma coluna de atualização de caução. Uma coluna de atualização de caução pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manter a consistência transacional.</p>
<ul>
<li><p>Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</p></li>
<li><p>Uma coluna de atualização de caução deve ser do tipo <strong>JET_coltypLong.</strong></p></li>
<li><p>Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</p></li>
<li><p>JET_bitColumnEscrowUpdate não pode ser usado em conjunto com as seguintes constantes:</p>
<ul>
<li><p>JET_bitColumnTagged</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>A coluna é criada sem uma versão. Outras transações que tentarem adicionar uma coluna com o mesmo nome falharão. Esse bit só é útil com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Ele não pode ser usado em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Use JET_bitColumnDeleteOnZero em vez de JET_bitColumnFinalize. JET_bitColumnFinalize especifica que uma coluna pode ser finalizada. Quando uma coluna que pode ser finalizada tem uma coluna de atualização de caução que chega a zero, a linha será excluída. As versões futuras podem invocar uma função de retorno de chamada em vez disso. Para obter mais informações, consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução. JET_bitColumnFinalize não pode ser usada com JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>O valor padrão de uma coluna é fornecido pela função de retorno de chamada, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. <strong>pvDefault</strong> deve apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve ser definido como sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p>
<p>JET_bitColumnUserDefinedDefault não pode ser usado em conjunto com as seguintes constantes:</p>
<ul>
<li><p>JET_bitColumnFixed</p></li>
<li><p>JET_bitColumnNotNULL</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
<li><p>JET_bitColumnUpdatable</p></li>
<li><p>JET_bitColumnEscrowUpdate</p></li>
<li><p>JET_bitColumnFinalize</p></li>
<li><p>JET_bitColumnDeleteOnZero</p></li>
<li><p>JET_bitColumnMaybeNull</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído. Um uso comum para uma coluna que pode ser finalizada é usá-lo como um campo de contagem de referência e, quando o campo atinge zero, o registro é excluído. JET_bitColumnDeleteOnZero está relacionado a JET_bitColumnFinalize. Uma coluna Delete-on-zero deve ser uma coluna de atualização de caução. JET_bitColumnDeleteOnZero não pode ser usada com JET_bitColumnFinalize. JET_bitColumnDeleteOnZero não pode ser usado com colunas padrão definidas pelo usuário.</p></td>
</tr>
</tbody>
</table>


**pvDefault**

Aponta para um buffer que será o valor padrão para uma coluna. O comprimento do buffer é **cbDefault**. Se não houver nenhum padrão, **pvDefault** deverá ser definido como NULL e **cbDefault** deverá ser definido como zero. Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma estrutura de JET_USERDEFINEDDEFAULT. Os valores padrão não podem ser maiores que 255 bytes. Se um valor padrão for maior que 255 bytes, ele será silenciosamente truncado.

**cbDefault**

O tamanho, em bytes, do buffer especificado por **pvDefault**.

**cp**

A página de código da coluna. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de zero significa que o padrão será usado (Inglês, 1252). Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.

**columnid**

Em caso de sucesso, o identificador de coluna da coluna recém-criada será passado de volta neste campo. Em caso de falha, o valor é indefinido.

**erra**

O campo **Err** conterá o status da criação desta coluna. Consulte [JetAddColumn](./jetaddcolumn-function.md) para obter uma lista de valores de retorno prováveis.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_COLUMNCREATE_W</strong> (Unicode) e <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
