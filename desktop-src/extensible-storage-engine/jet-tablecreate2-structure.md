---
description: 'Saiba mais sobre: estrutura JET_TABLECREATE2 dados'
title: Estrutura JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: 95e4d60ba80317624004fa7c9335005aa16a9300
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476462"
---
# <a name="jet_tablecreate2-structure"></a>Estrutura JET_TABLECREATE2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_tablecreate2-structure"></a>Estrutura JET_TABLECREATE2

A **JET_TABLECREATE2** contém as informações necessárias para criar uma tabela preenchida com colunas e índices em um banco de dados ESE e que designa uma função de retorno de chamada. A **JET_TABLECREATE2** estrutura é usada por [JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md)

**Windows XP:** A **estrutura JET_TABLECREATE2** é introduzida no Windows XP.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof( JET_TABLECREATE2 ) em bytes.

**szTableName**

O nome da tabela a ser criado.

O nome deve usar para atender às seguintes condições:

  - Ter um valor menor que JET_cbNameMost, sem incluir o NULL de terminação.

<!-- end list -->

  - Consiste no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto ponto de exclamação ( ), vírgula (,), colchete de abertura ( ) e colchete de fechamento ( ), ou seja, caracteres \! \[ ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio de 0x5a, 0x5c e 0x5d por meio \] 0x7f.

<!-- end list -->

  - Não comece com um espaço.

<!-- end list -->

  - Consiste em pelo menos um caractere sem espaço.

**szTemplateTableName**

O nome de uma tabela já existente da qual herdar DDL base (Linguagem de Definição de Dados). O uso de uma tabela de modelo permite a criação fácil de muitas tabelas com colunas e índices idênticos.

**ulPages**

O número inicial de páginas de banco de dados a ser alocada para a tabela. Especificar um número maior que um pode reduzir a fragmentação se muitas linhas são inseridas nesta tabela.

**ulDensity**

A densidade da tabela, em pontos percentuais. O número deve ser 0 ou no intervalo de 20 a 100. Passar 0 significa que o valor padrão deve ser usado. O padrão é 80.

**rgcolumncreate**

Uma matriz de [JET_COLUMNCREATE](./jet-columncreate-structure.md) estruturas, cada uma correspondendo a uma coluna a ser criada na nova tabela.

**Ccolumns**

o número de [JET_COLUMNCREATE](./jet-columncreate-structure.md) elementos em **rgcolumncreate**.

**rgindexcreate**

Uma matriz de [JET_INDEXCREATE](./jet-indexcreate-structure.md) estruturas, cada uma correspondendo a um índice a ser criado na nova tabela.

**cIndexes**

O número de [JET_INDEXCREATE](./jet-indexcreate-structure.md) elementos em **rgindexcreate**.

**szCallback**

A função que é chamada durante determinados eventos. **cbtyp** determina quando a função de retorno de chamada será chamada.

O formato **de szCallback** deve ser "função de módulo"— por exemplo, "alpha beta" refere-se à função beta no módulo \! chamado \! "alpha". O protótipo da função deve corresponder [JET_CALLBACK](./jet-callback-callback-function.md). Para obter mais informações, [consulte JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Descreve o tipo de função de retorno de chamada designada por **szCallback**. Para obter mais informações, [consulte JET_CBTYP](./jet-cbtyp.md). Esse campo de bits é composto por um ou mais dos bits a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>A função de retorno de chamada será chamada quando uma coluna que pode ser finalizada tiver passado para zero.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>A função de retorno de chamada será chamada antes da inserção do registro.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>A função de retorno de chamada será chamada depois que o mecanismo de banco de dados terminar de inserir um registro.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>A função de retorno de chamada será chamada antes da modificação de um registro.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>A função de retorno de chamada será chamada depois de concluir a modificação de um registro.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>A função de retorno de chamada será chamada antes da exclusão de um registro.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>A função de retorno de chamada será chamada depois que um registro tiver sido excluído.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>A função de retorno de chamada será chamada para calcular um padrão definido pelo usuário.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>A função de retorno de chamada será chamada após a conclusão de uma chamada para <a href="gg294095(v=exchg.10).md">JetDefragment2.</a></p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a um cursor deve ser liberado.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a uma tabela deve ser liberado.</p> | 



**grbit**

Um grupo de bits que contém as opções para essa chamada, que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Definir JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Definir JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo. Novas tabelas podem especificar o nome dessa tabela como sua tabela de modelo. Definir JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Deve ser usado em conjunto com JET_bitTableCreateTemplateTable. Preterido. Não use.</p> | 



**Tableid**

Um campo de saída que contém a [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for bem-sucedida. Se a chamada à API falhar, o valor será indefinido.

**cCreated**

Um campo de saída que contém a contagem de objetos criados se a chamada à API for bem-sucedida. Se a chamada à API falhar, o valor será indefinido.

A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_TABLECREATE2_W</strong> (Unicode) e <strong>JET_TABLECREATE2_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
