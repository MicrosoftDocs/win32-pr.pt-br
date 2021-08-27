---
description: 'Saiba mais sobre: estrutura de JET_TABLECREATE2'
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
ms.openlocfilehash: b4d84a21fc9115823eaff0716b90ee37f1ae6655
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988099"
---
# <a name="jet_tablecreate2-structure"></a>Estrutura JET_TABLECREATE2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_tablecreate2-structure"></a>Estrutura JET_TABLECREATE2

A estrutura de **JET_TABLECREATE2** contém as informações necessárias para criar uma tabela populada com colunas e índices em um banco de dados ESE e que designa uma função de retorno de chamada. A estrutura de **JET_TABLECREATE2** é usada pelo [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).

**Windows XP:** a estrutura de **JET_TABLECREATE2** é introduzida no Windows XP.

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

**cbStruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof (JET_TABLECREATE2) em bytes.

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

o número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) em **rgcolumncreate**.

**rgindexcreate**

Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas corresponde a um índice a ser criado na nova tabela.

**cIndexes**

O número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) em **rgindexcreate**.

**szCallback**

A função que é chamada durante determinados eventos. **cbtyp** determina quando a função de retorno de chamada será chamada.

O formato de **szCallback** deve ser "função do módulo \! " — por exemplo, "Alpha \! beta" refere-se à função beta no módulo chamado "Alpha". O protótipo da função deve corresponder a [JET_CALLBACK](./jet-callback-callback-function.md). Para obter mais informações, consulte [JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Descreve o tipo de função de retorno de chamada designado por **szCallback**. Para obter mais informações, consulte [JET_CBTYP](./jet-cbtyp.md). Este campo de bits é composto de um ou mais dos seguintes itens.


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
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>A função de retorno de chamada será chamada depois que uma chamada para <a href="gg294095(v=exchg.10).md">JetDefragment2</a> for concluída.</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a um cursor precisar ser liberado.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a uma tabela precisar ser liberado.</p> | 



**grbit**

Um grupo de bits que contém as opções para essa chamada, que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>A configuração JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>A configuração JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo. As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos. A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Deve ser usado em conjunto com JET_bitTableCreateTemplateTable. Preterido. Não use.</p> | 



**TableID**

Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

**cCreated**

Um campo de saída que contém a contagem de objetos que são criados se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

A contagem de objetos que é criada é igual à soma de colunas, tabelas e índices criados com êxito.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_TABLECREATE2_W</strong> (Unicode) <strong>e JET_TABLECREATE2_A</strong> (ANSI).</p> | 



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
