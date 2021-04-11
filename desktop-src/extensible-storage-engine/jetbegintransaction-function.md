---
description: 'Saiba mais sobre: função JetBeginTransaction'
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
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296182"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="24c8f-103">Função JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="24c8f-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="24c8f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="24c8f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="24c8f-105">Função JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="24c8f-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="24c8f-106">A função **JetBeginTransaction** faz com que uma sessão Insira uma transação e crie um novo ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="24c8f-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="24c8f-107">Essa função pode ser chamada mais de uma vez em uma única sessão para causar a criação de pontos de salvamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="24c8f-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="24c8f-108">Esses pontos de salvamento podem ser usados para manter ou descartar de forma seletiva as alterações no estado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="24c8f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24c8f-109">Parameters</span></span>

<span data-ttu-id="24c8f-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="24c8f-110">*sesid*</span></span>

<span data-ttu-id="24c8f-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="24c8f-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="24c8f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="24c8f-112">Return Value</span></span>

<span data-ttu-id="24c8f-113">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="24c8f-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="24c8f-114">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="24c8f-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24c8f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="24c8f-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="24c8f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="24c8f-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="24c8f-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="24c8f-118">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="24c8f-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="24c8f-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="24c8f-120">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="24c8f-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="24c8f-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="24c8f-122">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="24c8f-123">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="24c8f-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="24c8f-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="24c8f-125">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="24c8f-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="24c8f-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="24c8f-127">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="24c8f-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="24c8f-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="24c8f-129">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="24c8f-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="24c8f-130">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="24c8f-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="24c8f-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="24c8f-132">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="24c8f-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="24c8f-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="24c8f-134">Uma nova transação não pode ser iniciada porque a sessão já está na profundidade máxima de ponto de salvamento permitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="24c8f-135">Em caso de sucesso, a sessão fornecida estará dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="24c8f-136">Se a sessão estava anteriormente dentro de uma transação, um novo ponto de salvamento será criado.</span><span class="sxs-lookup"><span data-stu-id="24c8f-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="24c8f-137">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="24c8f-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="24c8f-138">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="24c8f-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="24c8f-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="24c8f-139">Remarks</span></span>

<span data-ttu-id="24c8f-140">O mecanismo de banco de dados fornece um modelo de isolamento de instantâneo para suas transações.</span><span class="sxs-lookup"><span data-stu-id="24c8f-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="24c8f-141">Isso significa que, quando uma sessão entra pela primeira vez em um estado transacional, a sessão verá todo o banco de dados congelado no início da transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="24c8f-142">Uma sessão não precisa ler nenhum dado de bloqueio porque ela sempre pode acessar a versão apropriada desses dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="24c8f-143">Isso significa que uma sessão que está atualizando dados nunca bloqueará a leitura desses dados em uma sessão diferente.</span><span class="sxs-lookup"><span data-stu-id="24c8f-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="24c8f-144">Outra implicação do uso de isolamento de instantâneo é o modelo de bloqueio usado para atualizações.</span><span class="sxs-lookup"><span data-stu-id="24c8f-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="24c8f-145">O mecanismo de banco de dados oferecerá um bloqueio de gravação em determinado dado para a primeira sessão que o solicita.</span><span class="sxs-lookup"><span data-stu-id="24c8f-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="24c8f-146">Esse bloqueio de gravação é liberado quando a transação é confirmada ou anulada completamente, de modo que a sessão não esteja mais em uma transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="24c8f-147">Enquanto uma sessão mantém um bloqueio de gravação, qualquer outra sessão que solicite o mesmo bloqueio de gravação não será bloqueada até que o bloqueio de gravação esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="24c8f-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="24c8f-148">Em vez disso, essa segunda sessão falhará imediatamente com JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="24c8f-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="24c8f-149">Para resolver esse conflito, a segunda sessão deve anular (ou confirmar) sua transação completamente, aguardar um pequeno período de tempo para a primeira sessão confirmar ou anular sua transação e iniciar tudo novamente.</span><span class="sxs-lookup"><span data-stu-id="24c8f-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="24c8f-150">Para dar suporte ao isolamento de instantâneo, o mecanismo de banco de dados armazena todas as versões de todos os dados modificados na memória desde o momento em que a transação ativa mais antiga em qualquer sessão foi iniciada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="24c8f-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="24c8f-151">Isso tem implicações importantes para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24c8f-151">This has important implications for your application.</span></span> <span data-ttu-id="24c8f-152">Qualquer comportamento que faça com que um grande número de versões para se acumular na memória pode fazer com que a instância esgotasse seu tamanho máximo de repositório de versão (consulte [JET_paramMaxVerPages](./resource-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="24c8f-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="24c8f-153">Esse comportamento inclui, mas não se limita a atualizações muito grandes em uma única transação e transações de execução muito longa.</span><span class="sxs-lookup"><span data-stu-id="24c8f-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="24c8f-154">Como resultado, é muito importante configurar corretamente o tamanho do repositório de versão para a carga transacional esperada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24c8f-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="24c8f-155">Também é importante tomar muito cuidado para limitar o número de atualizações executadas em uma única transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="24c8f-156">Além disso, é importante tornar as transações tão curtas quanto possível em cenários de alta carga.</span><span class="sxs-lookup"><span data-stu-id="24c8f-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="24c8f-157">É altamente recomendável que o aplicativo sempre esteja no contexto de uma transação ao chamar as APIs do ESE que recuperam ou atualizam dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="24c8f-158">Se isso não for feito, o mecanismo de banco de dados encapsulará automaticamente cada chamada à API do ESE desse tipo em uma transação em nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24c8f-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="24c8f-159">O custo dessas transações muito curtas pode ser somado rapidamente em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="24c8f-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="24c8f-160">O comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread a partir do momento em que a primeira chamada para **JetBeginTransaction** é feita até o momento em que a chamada de correspondência para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita.</span><span class="sxs-lookup"><span data-stu-id="24c8f-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="24c8f-161">Esse comportamento pode ser alterado para remover essa restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="24c8f-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="24c8f-162">O mecanismo de banco de dados também dá suporte a modificações de esquema transacionais.</span><span class="sxs-lookup"><span data-stu-id="24c8f-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="24c8f-163">Por exemplo, é possível iniciar uma nova transação, criar uma tabela, adicionar algumas colunas, criar um índice ou dois e, em seguida, anular a transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="24c8f-164">Os elementos de esquema que acabou de ser adicionados serão removidos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24c8f-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="24c8f-165">Também é possível misturar modificações de esquema e atualizações de banco de dados comuns na mesma transação.</span><span class="sxs-lookup"><span data-stu-id="24c8f-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="24c8f-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24c8f-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-167"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="24c8f-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="24c8f-168">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="24c8f-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-169"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="24c8f-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="24c8f-170">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="24c8f-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-171"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="24c8f-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="24c8f-172">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="24c8f-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c8f-173"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="24c8f-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="24c8f-174">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="24c8f-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c8f-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="24c8f-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="24c8f-176">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="24c8f-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="24c8f-177">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="24c8f-177">See Also</span></span>

[<span data-ttu-id="24c8f-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24c8f-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="24c8f-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="24c8f-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="24c8f-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="24c8f-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="24c8f-181">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="24c8f-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="24c8f-182">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="24c8f-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="24c8f-183">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="24c8f-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="24c8f-184">JetRollback</span><span class="sxs-lookup"><span data-stu-id="24c8f-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="24c8f-185">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="24c8f-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="24c8f-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="24c8f-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="24c8f-187">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="24c8f-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
