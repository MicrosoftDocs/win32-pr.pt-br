---
description: 'Saiba mais sobre: Função JetSetColumnDefaultValue'
title: Função JetSetColumnDefaultValue
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402326a34a0551262d453b93db2287c69a7160b3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469713"
---
# <a name="jetsetcolumndefaultvalue-function"></a>Função JetSetColumnDefaultValue


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetcolumndefaultvalue-function"></a>Função JetSetColumnDefaultValue

A **função JetSetColumnDefaultValue** pode ser usada para alterar o valor padrão de uma coluna existente.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Dbid*

O banco de dados a ser usado para essa chamada.

*szTableName*

O nome da tabela que contém a coluna que será afetada.

*szColumnName*

O nome da coluna cujo valor padrão será alterado.

*Pvdata*

O buffer de entrada que contém o novo valor padrão.

*cbData*

O tamanho do buffer de entrada que contém o novo valor padrão.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>O mesmo que JET_errNullInvalid.</p> | 
| <p>JET_errColumnInUse</p> | <p>Essa coluna especificada está atualmente em uso por um índice.</p><p><strong>JetSetColumnDefaultValue</strong> não pode alterar o valor padrão de uma coluna referenciada na definição de um índice. Isso porque fazer isso pode alterar o conteúdo do índice.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Essa coluna especificada não existe para esta tabela.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>A ID do banco de dados especificada era inválida.</p> | 
| <p>JET_errInvalidName</p> | <p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p><ul><li><p>Os nomes de objeto devem ser compostos de caracteres ASCII.</p></li><li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li><li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li><li><p>Os nomes de objeto podem não começar com um espaço.</p></li><li><p>Os nomes de objeto podem não conter caracteres de controle ASCII (0x00 por meio 0x1F).</p></li><li><p>Os nomes de objeto podem não conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou um caractere de colchete direito (]).</p></li><li><p>Depois de validada, somente a parte da cadeia de caracteres até o primeiro espaço (se algum) será usada para o nome do objeto. Isso significa que os nomes de objeto também podem não conter um espaço.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNullInvalid</p> | <p>Não foi possível definir a coluna como NULL. Isso acontece para <strong>JetSetColumnDefaultValue</strong> quando:</p><ul><li><p><em>cbData</em> é zero.</p></li><li><p><strong>pvData</strong> é NULL.</p></li></ul><p>Portanto, não é possível definir o valor padrão de uma coluna (de volta) como NULL ou com um valor de comprimento zero.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Essa tabela especificada não existe para esse banco de dados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTableInUse</p> | <p>Essa tabela especificada está em uso por outra sessão.</p><p><strong>JetSetColumnDefaultValue</strong> requer acesso exclusivo a uma tabela para alterar o valor padrão da coluna para versões anteriores ao Windows Server 2003.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>É ilegal tentar uma atualização quando estiver dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errWriteConflict</p> | <p>Outra sessão já travada o registro para atualização. A atualização tentada por esta sessão falhará.</p> | 



Em caso de êxito, o valor padrão da coluna especificada na tabela especificada no banco de dados especificado é alterado permanentemente para o novo valor padrão.

Em caso de falha, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Não é possível alterar o valor padrão de uma coluna em uma tabela de modelo.

O mecanismo de banco de dados truncará silenciosamente o valor padrão de uma coluna para 255 bytes para texto longo e colunas binárias longas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetSetColumnDefaultValueW</strong> (Unicode) e <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
