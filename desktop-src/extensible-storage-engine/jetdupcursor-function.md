---
description: 'Saiba mais sobre: função JetDupCursor'
title: Função JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 009b84837895ce13f63cc37e4b5b152f4274ee62
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985879"
---
# <a name="jetdupcursor-function"></a>Função JetDupCursor


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdupcursor-function"></a>Função JetDupCursor

A função **JetDupCursor** duplica um cursor Open e retorna um identificador para o cursor duplicado. Se o cursor que foi duplicado era um cursor somente leitura, o cursor duplicado também é um cursor somente leitura. Qualquer estado relacionado à construção de uma chave de pesquisa ou à atualização de um registro não é copiado para o cursor duplicado. Além disso, o local do cursor original não é duplicado no cursor duplicado. O cursor duplicado sempre é aberto no índice clusterizado e seu local está sempre na primeira linha da tabela.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*ptableid*

Ponteiro para *TableName*.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Não existem recursos de cursor disponíveis.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, *pTableID* é definido como um cursor duplicado.

Em caso de falha, nenhuma alteração é feita. O estado de *TableName* não foi alterado.

#### <a name="remarks"></a>Comentários

O cursor duplicado não tem o estado do cursor inteiro copiado. O local do cursor duplicado, incluindo o índice atual, geralmente é diferente do cursor fornecido. O cursor duplicado sempre é retornado no índice clusterizado e na primeira linha da tabela. Se a tabela estiver vazia, o cursor duplicado não estará em nenhuma linha.

As tabelas abertas com **JetDupCursor** normalmente devem ser fechadas com [JetCloseTable](./jetclosetable-function.md). A exceção a essa regra ocorre quando **JetDupCursor** é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)). Ao reverter uma transação, o cursor é fechado automaticamente. Nesse caso, é um erro fechar a tabela com [JetCloseTable](./jetclosetable-function.md).

O número de tabelas que podem ser abertas simultaneamente é afetado diretamente pelo [JET_paramMaxOpenTables](./resource-parameters.md). Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter detalhes.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
