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
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922662"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="add1c-103">Função JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="add1c-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="add1c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="add1c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="add1c-105">Função JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="add1c-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="add1c-106">A função **JetCommitTransaction** confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior.</span><span class="sxs-lookup"><span data-stu-id="add1c-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="add1c-107">Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="add1c-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="add1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="add1c-108">Parameters</span></span>

<span data-ttu-id="add1c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="add1c-109">*sesid*</span></span>

<span data-ttu-id="add1c-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="add1c-110">The session to use for this call.</span></span>

<span data-ttu-id="add1c-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="add1c-111">*grbit*</span></span>

<span data-ttu-id="add1c-112">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="add1c-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="add1c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="add1c-113">Value</span></span></p></th>
<th><p><span data-ttu-id="add1c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="add1c-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="add1c-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="add1c-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="add1c-116">A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="add1c-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="add1c-117">Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade.</span><span class="sxs-lookup"><span data-stu-id="add1c-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="add1c-118">Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para <a href="gg294068(v=exchg.10).md">JetInit</a>.</span><span class="sxs-lookup"><span data-stu-id="add1c-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="add1c-119">Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit forem especificadas, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="add1c-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="add1c-120">Se essa chamada para <strong>JetCommitTransaction</strong> não corresponder à primeira chamada para <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para essa sessão, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="add1c-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="add1c-121">Isso acontece porque a ação final que ocorre no ponto de salvamento mais externo é o fator determinante em que toda a transação está realmente comprometida com o disco.</span><span class="sxs-lookup"><span data-stu-id="add1c-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="add1c-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="add1c-123">Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="add1c-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="add1c-124">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="add1c-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="add1c-125">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="add1c-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="add1c-126">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="add1c-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="add1c-127">Essa opção só está disponível a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="add1c-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="add1c-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="add1c-129">Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="add1c-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="add1c-130">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="add1c-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="add1c-131">Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</span><span class="sxs-lookup"><span data-stu-id="add1c-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="add1c-132">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="add1c-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="add1c-133">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="add1c-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="add1c-134">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="add1c-134">Return Value</span></span>

<span data-ttu-id="add1c-135">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="add1c-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="add1c-136">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="add1c-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="add1c-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="add1c-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="add1c-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="add1c-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="add1c-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="add1c-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="add1c-140">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="add1c-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="add1c-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="add1c-142">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="add1c-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="add1c-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="add1c-144">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="add1c-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="add1c-145">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="add1c-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="add1c-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="add1c-147">Uma das opções solicitadas era inválida ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="add1c-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="add1c-148">Esse erro será retornado por <strong>JetCommitTransaction</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="add1c-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="add1c-149">Um <em>grbit</em> inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="add1c-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="add1c-150">JET_bitWaitLastLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="add1c-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="add1c-151">JET_bitWaitAllLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="add1c-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="add1c-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="add1c-153">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="add1c-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="add1c-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="add1c-155">A operação falhou porque a sessão especificada não está em uma transação.</span><span class="sxs-lookup"><span data-stu-id="add1c-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="add1c-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="add1c-157">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="add1c-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="add1c-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="add1c-159">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="add1c-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="add1c-160">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="add1c-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="add1c-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="add1c-162">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="add1c-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="add1c-163">Em caso de sucesso, as alterações feitas no banco de dados durante o ponto de salvamento atual para a sessão especificada serão confirmadas e o ponto de salvamento será encerrado.</span><span class="sxs-lookup"><span data-stu-id="add1c-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="add1c-164">Se o último ponto de salvamento para a sessão foi finalizado, a transação será, opcionalmente, liberada para o arquivo de log de transações e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="add1c-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="add1c-165">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="add1c-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="add1c-166">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="add1c-166">No change to the database state will occur.</span></span> <span data-ttu-id="add1c-167">O aplicativo deve chamar [JetRollback](./jetrollback-function.md) para anular a transação.</span><span class="sxs-lookup"><span data-stu-id="add1c-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="add1c-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="add1c-168">Remarks</span></span>

<span data-ttu-id="add1c-169">Deve haver uma chamada para **JetCommitTransaction** ou [JetRollback](./jetrollback-function.md) para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.</span><span class="sxs-lookup"><span data-stu-id="add1c-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="add1c-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add1c-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="add1c-171"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-172">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="add1c-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-173"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-174">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="add1c-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-175"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-176">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="add1c-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-177"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-178">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="add1c-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-180">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="add1c-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="add1c-181">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="add1c-181">See Also</span></span>

[<span data-ttu-id="add1c-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="add1c-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="add1c-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="add1c-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="add1c-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="add1c-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="add1c-185">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="add1c-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="add1c-186">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="add1c-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="add1c-187">JetRollback</span><span class="sxs-lookup"><span data-stu-id="add1c-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="add1c-188">JetStopService</span><span class="sxs-lookup"><span data-stu-id="add1c-188">JetStopService</span></span>](./jetstopservice-function.md)
