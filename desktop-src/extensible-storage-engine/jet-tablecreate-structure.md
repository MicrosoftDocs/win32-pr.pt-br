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
ms.openlocfilehash: 92695b9600ef18e716fa02cf58157c3c4781988e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468353"
---
# <a name="jet_tablecreate-structure"></a>Estrutura JET_TABLECREATE


_**Aplica-se a:** Windows | Windows Servidor_

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>A configuração JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>A configuração JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo. As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos. A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Preterido. Não use.</p> | 



**TableID**

Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

**cCreated**

Um campo de saída que contém a contagem de objetos criados se a chamada à API for realizada com sucesso. Se a chamada à API falhar, o valor será indefinido.

A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_TABLECREATE_W</strong> (Unicode) e <strong>JET_TABLECREATE_A</strong> (ANSI).</p> | 



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
