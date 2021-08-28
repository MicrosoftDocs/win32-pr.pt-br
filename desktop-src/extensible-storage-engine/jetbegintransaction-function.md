---
description: 'Saiba mais sobre: Função JetBeginTransaction'
title: Função JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 991f80ab346ae039c6222a508374de806d0faf2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479262"
---
# <a name="jetbegintransaction-function"></a>Função JetBeginTransaction


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbegintransaction-function"></a>Função JetBeginTransaction

A **função JetBeginTransaction** faz com que uma sessão insira uma transação e crie um novo ponto de salvar. Essa função pode ser chamada mais de uma vez em uma única sessão para causar a criação de pontos de economia adicionais. Esses pontos de salvar podem ser usados para manter ou descartar seletivamente as alterações no estado do banco de dados.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Uma nova transação não pode ser iniciada porque a sessão já está na profundidade máxima do ponto de salvar permitida pelo mecanismo de banco de dados.</p> | 



Em caso de êxito, a sessão fornecida estará dentro de uma transação. Se a sessão estava anteriormente dentro de uma transação, um novo ponto de salvar será criado.

Em caso de falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

O mecanismo de banco de dados fornece um modelo de isolamento de instantâneo para suas transações. Isso significa que, quando uma sessão entrar pela primeira vez em um estado transacional, a sessão verá todo o banco de dados congelado no tempo no início da transação. Uma sessão não precisa ler nenhum bloqueio de dados porque ela sempre pode acessar a versão apropriada desses dados. Isso significa que uma sessão que está atualizando dados nunca impedirá que uma sessão diferente leia esses dados.

Outra implicação do uso do isolamento de instantâneo é o modelo de bloqueio usado para atualizações. O mecanismo de banco de dados receberá um bloqueio de gravação em determinado dado de dados para a primeira sessão que o solicitar. Esse bloqueio de gravação é liberado quando a transação é comprometida ou anulada completamente, de forma que a sessão não está mais em uma transação. Enquanto uma sessão mantém um bloqueio de gravação, qualquer outra sessão que solicita o mesmo bloqueio de gravação não será bloqueado até que o bloqueio de gravação seja disponibilizado. Em vez disso, essa segunda sessão falhará imediatamente com JET_errWriteConflict. Para resolver esse conflito, a segunda sessão deve anular (ou fazer commit) de sua transação completamente, aguardar um pequeno período de tempo para que a primeira sessão commit ou aborte sua transação e, em seguida, iniciar tudo novamente.

Para dar suporte ao isolamento de instantâneo, o mecanismo de banco de dados armazena todas as versões de todos os dados modificados na memória desde a hora em que a transação ativa mais antiga em qualquer sessão foi iniciada pela primeira vez. Isso tem implicações importantes para seu aplicativo. Qualquer comportamento que faz com que um grande número de versões seja construído na memória pode fazer com que a instância escareje seu tamanho máximo do armazenamento de versão (consulte [JET_paramMaxVerPages](./resource-parameters.md) em [Parâmetros](./extensible-storage-engine-system-parameters.md) do Sistema para obter mais informações). Esse comportamento inclui, mas não está limitado a atualizações muito grandes em uma única transação e transações de execução muito longa. Como resultado, é muito importante configurar corretamente o tamanho do armazenamento de versão para a carga transacional esperada do aplicativo. Também é importante ter muito cuidado para limitar o número de atualizações executadas em uma única transação. Além disso, é importante tornar as transações tão curtas quanto possível em cenários de alta carga.

É altamente recomendável que o aplicativo sempre está no contexto de uma transação ao chamar APIs ESE que recuperam ou atualizam dados. Se isso não for feito, o mecanismo de banco de dados envolverá automaticamente cada chamada à API do ESE desse tipo em uma transação em nome do aplicativo. O custo dessas transações muito curtas pode ser somdo rapidamente em alguns casos.

O comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread desde o momento em que a primeira chamada para **JetBeginTransaction** é feita até o momento em que a chamada correspondente para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita. Esse comportamento pode ser alterado para remover essa restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

O mecanismo de banco de dados também dá suporte a modificações de esquema transacional. Por exemplo, é possível iniciar uma nova transação, criar uma tabela, adicionar algumas colunas, criar um índice ou duas e, em seguida, anular a transação. Os elementos de esquema que foram adicionados serão removidos do banco de dados. Também é possível combinar modificações de esquema e atualizações comuns de banco de dados na mesma transação.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
