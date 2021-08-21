---
description: 'Saiba mais sobre: Função JetCommitTransaction2'
title: Função JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ad6c3584f27421b14ef44ed86b423778a570b63
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465843"
---
# <a name="jetcommittransaction2-function"></a>Função JetCommitTransaction2


_**Aplica-se a:** Windows | Windows Servidor_

A **função JetCommitTransaction2** confirma as alterações feitas no estado do banco de dados durante o ponto de economia atual e as migra para o ponto de economia anterior. Se o ponto de economia mais externo for confirmado, as alterações feitas durante esse ponto de salvar serão comprometidas no estado do banco de dados e a sessão sairá da transação.

A **função JetCommitTransaction2** foi introduzida no Windows 8 operacional.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*grbit*

Um grupo de bits que especificam zero ou mais dos valores listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>A transação é comprometida normalmente, mas essa API não aguarda a liberação da transação para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação às custas da durabilidade. Qualquer transação que não for liberado para o log antes de uma falha será anulada automaticamente durante a recuperação de falha durante a próxima chamada para a <a href="gg294068(v=exchg.10).md">função JetInit.</a></p><p>Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit for especificado, essa opção será ignorada.</p><p>Se essa chamada para <strong>JetCommitTransaction2</strong> não corresponder à primeira chamada à função <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para esta sessão, essa opção será ignorada. Isso ocorre porque a ação final que ocorre no ponto de economia mais externo é o fator determinante em se toda a transação está realmente comprometida no disco.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberados para o arquivo de log de transações serão liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador.</p><p>Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação.</p><p>Essa opção não pode ser usada em combinação com qualquer outra opção.</p><p>Essa opção está disponível em versões do sistema operacional Windows Server a partir do Windows Server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Se a sessão tiver confirmado transações anteriormente e elas ainda não foram liberados para o arquivo de log de transações, elas deverão ser liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador. Isso será útil se o aplicativo já tiver confirmado várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</p><p>Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação.</p><p>Essa opção não pode ser usada em combinação com qualquer outra opção.</p> | 



*cmsecDurableCommit*

A duração para fazer commit de uma transação lento.

*pCommitID*

A ID de confirmação associada a esse registro de confirmação.

### <a name="return-value"></a>Valor retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE (Extensible Armazenamento Engine), consulte [Extensible Armazenamento Engine Error](./extensible-storage-engine-errors.md) [Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para a <a href="gg269240(v=exchg.10).md">função JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por versões do sistema operacional Windows a partir do Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma das opções solicitadas era inválida ou não implementada. Esse erro será retornado pela função <strong>JetCommitTransaction2</strong> quando ocorrer o seguinte:</p><ul><li><p>Um <em>grbit ilegal</em> é especificado.</p></li><li><p>JET_bitWaitLastLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNotInTransaction</p> | <p>A operação falhou porque a sessão determinada não está em uma transação.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>Esse erro só será retornado por versões do sistema operacional Windows a partir do Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, todas as alterações feitas no banco de dados durante o ponto de economia atual para a sessão determinada serão confirmados e esse ponto de salvar será encerrado. Se o último ponto de salvar para a sessão tiver sido encerrado, a transação será, opcionalmente, liberado para o arquivo de log de transações e a sessão sairá da transação.

Em caso de falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá. O aplicativo deve chamar a [função JetRollback](./jetrollback-function.md) para anular a transação.

#### <a name="remarks"></a>Comentários

Deve haver uma chamada para **JetCommitTransaction2** ou [JetRollback](./jetrollback-function.md) para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Confira também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
