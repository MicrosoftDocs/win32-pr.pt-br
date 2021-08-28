---
description: 'Saiba mais sobre: estrutura JET_TABLECREATE3 dados'
title: Estrutura JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b3e1f3a21b5e5f901ef039b9cff0cdd52d415d5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983019"
---
# <a name="jet_tablecreate3-structure"></a>Estrutura JET_TABLECREATE3


_**Aplica-se a:** Windows | Windows Servidor_

A **estrutura JET_TABLECREATE3** contém as informações necessárias para criar uma tabela preenchida com colunas e índices em um banco de dados ESE (Extensible Armazenamento Engine) e que designa uma função de retorno de chamada. A **JET_TABLECREATE3** estrutura é usada pela [função JetCreateTableColumnIndex3.](./jetcreatetablecolumnindex3-function.md)

A **JET_TABLECREATE3** foi introduzida no sistema operacional Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof( JET_TABLECREATE3 ) em bytes.

**szTableName**

O nome da tabela a ser criada.

O nome deve atender às seguintes condições:

  - Ele deve ter um valor menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ele deve consistir no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto ponto de exclamação ( ), vírgula (,), colchete de abertura ( ) e colchete de fechamento ( ); ou seja, caracteres \! \[ ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio de 0x5a, 0x5c e \] 0x5d 0x7f.

  - Ele não deve começar com um espaço.

  - Ele deve consistir em pelo menos um caractere sem espaço.

**szTemplateTableName**

O nome de uma tabela existente da qual herdar a DDL (linguagem de definição de dados base). O uso de uma tabela de modelo permite a fácil criação de muitas tabelas com colunas e índices idênticos.

**ulPages**

O número inicial de páginas de banco de dados a ser alocada para a tabela. Especificar um número maior que um pode reduzir a fragmentação se muitas linhas são inseridas nesta tabela.

**ulDensity**

A densidade da tabela, em pontos percentuais. O número deve ser 0 ou no intervalo de 20 a 100. Passar 0 significa que o valor padrão deve ser usado. O valor padrão é 80.

**rgcolumncreate**

Uma matriz de [JET_COLUMNCREATE](./jet-columncreate-structure.md) estruturas, cada uma correspondendo a uma coluna a ser criada na nova tabela.

**Ccolumns**

O número de [JET_COLUMNCREATE](./jet-columncreate-structure.md) no *parâmetro rgcolumncreate.*

**rgindexcreate**

Uma matriz de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) estruturas, cada uma correspondendo a um índice a ser criado na nova tabela.

**cIndexes**

O número de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) no *parâmetro rgindexcreate.*

**szCallback**

A função que é chamada durante determinados eventos. **cbtyp** determina quando a função de retorno de chamada será chamada.

O formato **de szCallback** deve ser "função de módulo", por exemplo, "alpha beta" refere-se à função beta no módulo \! chamado \! "alpha".

O protótipo da função deve corresponder à função [JET_CALLBACK](./jet-callback-callback-function.md) retorno de chamada.

**cbtyp**

Descreve o tipo de função de retorno de chamada designada por **szCallback**. Para obter mais informações, [consulte JET_CBTYP](./jet-cbtyp.md).

Esse campo de bits é composto por um ou mais dos valores de bit listados na tabela a seguir.


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
| <p>JET_cbtypFreeCursorLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a um cursor deve ser liberado.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>A função de retorno de chamada será chamada quando o armazenamento local associado a uma tabela deve ser liberado.</p> | 



**grbit**

Um grupo de bits que contém zero ou mais dos valores de opção de chamada listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Impede operações DDL na tabela (como adicionar ou remover colunas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Faz com que a tabela seja uma tabela de modelo. Novas tabelas podem especificar o nome dessa tabela como sua tabela de modelo. Definir JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Deve ser usado em conjunto com JET_bitTableCreateTemplateTable. Preterido. Não use.</p> | 



**pSeqSpacehints**

Um ponteiro para uma [estrutura JET_SPACEHINTS](./jet-spacehints-structure.md) para índice sequencial padrão.

**pSeqSpacehints** foi introduzido no Windows 7.

**pLVSpacehints**

Um ponteiro para uma [estrutura JET_SPACEHINTS](./jet-spacehints-structure.md) para uma árvore valores longos separados.

**pLVSpacehints** foi introduzido no Windows 7.

**cbSeparateLV**

O tamanho para separar um LV intrínseco do registro primário. Qualquer estrutura C de valor longo para uma árvore LV separada. Para obter mais informações, consulte ng-value em [JET_SPACEHINTS](./jet-spacehints-structure.md). Colunas de valor longo menores que esse valor poderão ser separadas se o registro se tornar muito grande.

**cbSeparateLV** foi introduzido no Windows 7.

**Tableid**

Um campo de saída que contém a [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for bem-sucedida. Se a chamada à API falhar, o valor será indefinido. Essa tabela é aberta exclusivamente.

**cCreated**

Um campo de saída que contém a contagem de objetos criados se a chamada à API for bem-sucedida. Se a chamada à API falhar, o valor será indefinido.

A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_TABLECREATE3_W</strong> (Unicode) <strong>e JET_TABLECREATE3_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte também

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
