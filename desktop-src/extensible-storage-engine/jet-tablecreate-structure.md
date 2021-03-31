---
description: 'Saiba mais sobre: estrutura de JET_TABLECREATE'
title: Estrutura JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089888"
---
# <a name="jet_tablecreate-structure"></a>Estrutura JET_TABLECREATE


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_tablecreate-structure"></a>Estrutura JET_TABLECREATE

A estrutura de **JET_TABLECREATE** contém as informações necessárias para criar uma tabela populada com colunas e índices em um banco de dados ESE. A estrutura de **JET_TABLECREATE** é usada pelo [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof (JET_TABLECREATE) em bytes.

**szTableName**

O nome da tabela a ser criada.

O nome deve usar atender às seguintes condições:

  - Ter um valor menor que JET_cbNameMost, não incluindo o nulo de terminação.

<!-- end list -->

  - Consiste no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ), ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.

<!-- end list -->

  - Não comece com um espaço.

<!-- end list -->

  - Consistir em pelo menos um caractere que não seja de espaço.

**szTemplateTableName**

O nome de uma tabela já existente da qual herdar DDL base (linguagem de definição de dados). O uso de uma tabela de modelo permite a fácil criação de muitas tabelas com colunas e índices idênticos.

**ulPages**

O número inicial de páginas de banco de dados a serem alocadas para a tabela. A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.

**ulDensity**

A densidade da tabela, em pontos percentuais. O número deve ser 0 ou estar no intervalo de 20 a 100. Passar 0 significa que o valor padrão deve ser usado. O padrão é 80.

**rgcolumncreate**

Uma matriz de estruturas [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada uma correspondendo a uma coluna a ser criada na nova tabela.

**cColumns**

O número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) em **rgcolumncreate**.

**rgindexcreate**

Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas corresponde a um índice a ser criado na nova tabela.

**cIndexes**

O número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) em **rgindexcreate**.

**grbit**

Um grupo de bits que contém as opções para essa chamada, que incluem zero ou mais dos valores a seguir.

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>A configuração JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>A configuração JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo. As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos. A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Preterido. Não use.</p></td>
</tr>
</tbody>
</table>


**TableID**

Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

**cCreated**

Um campo de saída que contém a contagem de objetos criados se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.

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
<td><p>Implementado como <strong>JET_TABLECREATE_W</strong> (Unicode) e <strong>JET_TABLECREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
