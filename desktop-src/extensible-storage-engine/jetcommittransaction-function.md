---
description: 'Saiba mais sobre: função JetCommitTransaction'
title: Função JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b19e193fa0dc911112d0bd8ed8e672de6fc57a2b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983529"
---
# <a name="jetcommittransaction-function"></a>Função JetCommitTransaction


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcommittransaction-function"></a>Função JetCommitTransaction

A função **JetCommitTransaction** confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior. Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade. Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para <a href="gg294068(v=exchg.10).md">JetInit</a>.</p><p>Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit forem especificadas, essa opção será ignorada.</p><p>Se essa chamada para <strong>JetCommitTransaction</strong> não corresponder à primeira chamada para <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para essa sessão, essa opção será ignorada. Isso acontece porque a ação final que ocorre no ponto de salvamento mais externo é o fator determinante em que toda a transação está realmente comprometida com o disco.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</p><p>Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</p><p>Essa opção não pode ser usada em combinação com nenhuma outra opção.</p><p>essa opção só está disponível a partir do Windows Server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador. Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</p><p>Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</p><p>Essa opção não pode ser usada em combinação com nenhuma outra opção.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma das opções solicitadas era inválida ou não foi implementada. Esse erro será retornado por <strong>JetCommitTransaction</strong> quando:</p><ul><li><p>Um <em>grbit</em> inválido foi especificado.</p></li><li><p>JET_bitWaitLastLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNotInTransaction</p> | <p>A operação falhou porque a sessão especificada não está em uma transação.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, as alterações feitas no banco de dados durante o ponto de salvamento atual para a sessão especificada serão confirmadas e o ponto de salvamento será encerrado. Se o último ponto de salvamento para a sessão foi finalizado, a transação será, opcionalmente, liberada para o arquivo de log de transações e a sessão sairá da transação.

Se houver falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá. O aplicativo deve chamar [JetRollback](./jetrollback-function.md) para anular a transação.

#### <a name="remarks"></a>Comentários

Deve haver uma chamada para **JetCommitTransaction** ou [JetRollback](./jetrollback-function.md) para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
