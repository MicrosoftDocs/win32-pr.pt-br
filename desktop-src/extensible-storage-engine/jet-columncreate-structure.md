---
description: 'Saiba mais sobre: estrutura JET_COLUMNCREATE dados'
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
ms.openlocfilehash: ffe79dde0f24e82aa7ca9457604ea76b587e9b29
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984019"
---
# <a name="jet_columncreate-structure"></a>Estrutura JET_COLUMNCREATE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columncreate-structure"></a>Estrutura JET_COLUMNCREATE

A **JET_COLUMNCREATE** estrutura descreve uma coluna a ser criado em um banco de dados.

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

**Cbstruct**

O tamanho da estrutura, em bytes. Esse campo deve ser inicializado para **sizeof( JET_COLUMNCREATE )**.

**szColumnName**

O nome da coluna a ser criado. O nome deve atender aos seguintes critérios:

  - Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o NULL de terminação.

<!-- end list -->

  - Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto ponto de exclamação ( ), vírgula (,), colchete de abertura ( ) e colchete de fechamento ( ), ou seja, caracteres ASCII 0x20, 0x22 por meio de \! \[ \] 0x2d, 0x2f 0x5a, 0x5c, 0x5d 0x7f.

<!-- end list -->

  - Ele não pode começar com um espaço.

<!-- end list -->

  - Ele deve conter pelo menos um caractere sem espaço.

**coltyp**

O tipo da coluna (por exemplo, texto, binário ou numérico). Para obter mais informações, [consulte JET_COLTYP](./jet-coltyp.md).

**cbMax**

O comprimento máximo, em bytes, de uma coluna de comprimento variável. O comprimento da coluna para colunas de comprimento fixo.

**grbit**

Um grupo de bits que contém as opções para essa estrutura e que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>A coluna é fixa. Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente de quantos dados estão sendo armazenados na coluna. JET_bitColumnFixed pode ser usado com JET_bitColumnTagged. Esse bit não pode ser usado com valores longos, <strong>como JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>A coluna é marcada. As colunas marcadas não assumirão nenhum espaço no banco de dados se não contêm dados. Esse bit não pode ser usado com JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>A coluna nunca deve ser definida como um valor NULL.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>A coluna é incrementada automaticamente. O número é um número crescente e tem a garantia de ser exclusivo em uma tabela. No entanto, o número pode não ser contínuo. Por exemplo, se cinco linhas são inseridas em uma tabela, a coluna de decremento automático pode conter os valores { 1, 2, 6, 7, 8 }.</p><p><strong>Windows 2000:</strong> Esse bit pode ser usado somente em colunas do tipo <strong>JET_coltypLong</strong>.</p><p><strong>Windows Server 2003 e posterior:</strong> Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Esse bit é válido somente em chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo.</a></p> | 
| <p>JET_bitColumnTTKey</p> | <p>Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>A coluna pode ter vários valores. Uma coluna com vários valores pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com vários valores são identificados pelo membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ser colunas de comprimento fixo ou de comprimento variável.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>A coluna é uma coluna de atualização de escrow. Uma coluna de atualização de escrow pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manter a consistência transacional.</p><ul><li><p>Uma coluna de atualização de escrow só pode ser criada quando a tabela está vazia.</p></li><li><p>Uma coluna de atualização de escrow deve ser do <strong>tipo JET_coltypLong.</strong></p></li><li><p>Uma coluna de atualização de escrow deve ter um valor padrão (ou <strong>seja, cbDefault</strong> deve ser positivo).</p></li><li><p>JET_bitColumnEscrowUpdate pode ser usado em conjunto com as seguintes constantes:</p><ul><li><p>JET_bitColumnTagged</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li></ul></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>A coluna é criada sem uma versão. Outras transações que tentam adicionar uma coluna com o mesmo nome falharão. Esse bit só é útil com <a href="gg294122(v=exchg.10).md">JetAddColumn.</a> Ele não pode ser usado em uma transação.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Use JET_bitColumnDeleteOnZero em vez de JET_bitColumnFinalize. JET_bitColumnFinalize especifica que uma coluna pode ser finalizada. Quando uma coluna que pode ser finalizada tiver uma coluna de atualização de escrow que atinja zero, a linha será excluída. Versões futuras podem invocar uma função de retorno de chamada. Para obter mais informações, <a href="gg294098(v=exchg.10).md">consulte JET_CALLBACK</a>. Uma coluna que pode ser finalizada deve ser uma coluna de atualização de escrow. JET_bitColumnFinalize pode ser usado com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>O valor padrão de uma coluna é fornecido pela função de retorno de chamada, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. <strong>pvDefault deve</strong> apontar para uma <a href="gg269200(v=exchg.10).md">estrutura JET_USERDEFINEDDEFAULT,</a> e <strong>cbDefault</strong> deve ser definido como sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p><p>JET_bitColumnUserDefinedDefault pode ser usado em conjunto com as seguintes constantes:</p><ul><li><p>JET_bitColumnFixed</p></li><li><p>JET_bitColumnNotNULL</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li><li><p>JET_bitColumnUpdatable</p></li><li><p>JET_bitColumnEscrowUpdate</p></li><li><p>JET_bitColumnFinalize</p></li><li><p>JET_bitColumnDeleteOnZero</p></li><li><p>JET_bitColumnMaybeNull</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>A coluna é uma coluna de atualização de escrow e, quando atingir zero, o registro será excluído. Um uso comum para uma coluna que pode ser finalizada é usá-la como um campo de contagem de referência e quando o campo atinge zero, o registro é excluído. JET_bitColumnDeleteOnZero está relacionado a JET_bitColumnFinalize. Uma coluna delete-on-zero deve ser uma coluna de atualização de escrow. JET_bitColumnDeleteOnZero pode ser usado com JET_bitColumnFinalize. JET_bitColumnDeleteOnZero pode ser usado com colunas padrão definidas pelo usuário.</p> | 



**pvDefault**

Aponta para um buffer que será o valor padrão de uma coluna. O comprimento do buffer é **cbDefault.** Se não houver nenhum padrão, **pvDefault** deverá ser definido como NULL e **cbDefault** deverá ser definido como zero. Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma estrutura JET_USERDEFINEDDEFAULT configuração. Os valores padrão não podem ser maiores que 255 bytes. Se um valor padrão for maior que 255 bytes, ele será silenciosamente truncado.

**cbDefault**

O tamanho, em bytes, do buffer especificado por **pvDefault.**

**cp**

A página de código da coluna. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de zero significa que o padrão será usado (inglês, 1252). Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.

**Columnid**

Em caso de êxito, o identificador de coluna da coluna recém-criada será passado novamente nesse campo. Em caso de falha, o valor é indefinido.

**Err**

O **campo err** conterá o status da criação dessa coluna. Consulte [JetAddColumn para](./jetaddcolumn-function.md) ver uma lista de valores de retorno prováveis.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_COLUMNCREATE_W</strong> (Unicode) <strong>e JET_COLUMNCREATE_A</strong> (ANSI).</p> | 



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
