---
description: 'Saiba mais sobre: Função JetGetLock'
title: Função JetGetLock
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51509f4027d4748f32b8c9dfb8756433b5f93935
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984829"
---
# <a name="jetgetlock-function"></a>Função JetGetLock


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetlock-function"></a>Função JetGetLock

A **função JetGetLock** fornece um meio de reservar explicitamente a capacidade de atualizar uma linha, um bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura. Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas. Bloqueios de leitura geralmente não são necessários devido ao registro de versão. No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização ou garantir que uma operação subsequente seja bem-sucedida em virtude de que os bloqueios necessários já foram feitos.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão que será usada para essa chamada.

*Tableid*

O cursor que será usado para essa chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada, que incluem zero ou mais dos seguintes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReadLock</p> | <p>Esse sinalizador faz com que um bloqueio de leitura seja adquirido no registro atual. Bloqueios de leitura são incompatíveis com bloqueios de gravação já mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos por outras sessões.</p> | 
| <p>JET_bitWriteLock</p> | <p>Esse sinalizador faz com que um bloqueio de gravação seja adquirido no registro atual. Bloqueios de gravação não são compatíveis com bloqueios de gravação ou leitura mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos pela mesma sessão.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>O <em>grbit determinado</em> não é JET_bitReadLock ou JET_bitWriteLock. Deve ser um desses dois sinalizadores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor deve estar em um registro para adquirir um bloqueio. Bloqueios estão sempre em registros.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Bloqueios só podem ser adquiridos por sessões em uma transação.</p> | 
| <p>JET_errPermissionDenied</p> | <p>O cursor não pode ser somente leitura e adquirir um bloqueio de gravação.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A sessão deve ter permissões de gravação para adquirir o bloqueio de gravação.</p> | 
| <p>JET_errWriteConflict</p> | <p>O erro retornado quando um bloqueio conflitante é solicitado.</p> | 



Em caso de êxito, a sessão adquiriu o bloqueio solicitado.

Em caso de falha, a sessão não adquiriu o bloqueio solicitado.

#### <a name="remarks"></a>Comentários

Os bloqueios de gravação não podem ser adquiridos com sessões ou cursores que têm permissões somente leitura, mesmo que a sessão e o cursor não executem uma operação de atualização. A sessão e o cursor devem ter privilégios de gravação para adquirir um bloqueio de gravação.

Bloqueios de leitura e gravação são um meio de bloqueio pessimista. O bloqueio pessimista espera que várias sessões simultâneas entre em conflito e adquira bloqueios com antecedência para garantir que suas operações são bem-sucedidas.

A maioria das operações será serializável em virtude de bloqueios implicitamente feitos. No entanto, algumas operações não serão. Para ilustrar isso, considere as duas transações,

T1: R(A), U(B)

T2: R(B), U(A)

O versionamento de nível de registro garantirá que cada transação quando executada simultaneamente verá os valores originais para A e B. Não há nenhuma ordem serial de execução que possa produzir os mesmos resultados para A e B no caso de os resultados dependerem dos dados lidos. Para que o aplicativo torna essa transação serializável, ele deve adquirir um bloqueio de leitura explícito em A e B em cada transação quando o valor for lido.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
