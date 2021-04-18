---
description: 'Saiba mais sobre: função JetCommitTransaction2'
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
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812362"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="da1f3-103">Função JetCommitTransaction2</span><span class="sxs-lookup"><span data-stu-id="da1f3-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="da1f3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da1f3-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="da1f3-105">A função **JetCommitTransaction2** confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior.</span><span class="sxs-lookup"><span data-stu-id="da1f3-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="da1f3-106">Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="da1f3-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="da1f3-107">A função **JetCommitTransaction2** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da1f3-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="da1f3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da1f3-108">Parameters</span></span>

<span data-ttu-id="da1f3-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="da1f3-109">*sesid*</span></span>

<span data-ttu-id="da1f3-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-110">The session to use for this call.</span></span>

<span data-ttu-id="da1f3-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="da1f3-111">*grbit*</span></span>

<span data-ttu-id="da1f3-112">Um grupo de bits que especifica zero ou mais valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da1f3-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da1f3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="da1f3-113">Value</span></span></p></th>
<th><p><span data-ttu-id="da1f3-114">Significado</span><span class="sxs-lookup"><span data-stu-id="da1f3-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="da1f3-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="da1f3-116">A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="da1f3-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="da1f3-117">Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade.</span><span class="sxs-lookup"><span data-stu-id="da1f3-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="da1f3-118">Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para a função <a href="gg294068(v=exchg.10).md">JetInit</a> .</span><span class="sxs-lookup"><span data-stu-id="da1f3-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="da1f3-119">Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit forem especificadas, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="da1f3-120">Se essa chamada para <strong>JetCommitTransaction2</strong> não corresponder à primeira chamada para a função <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para essa sessão, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="da1f3-121">Isso acontece porque a ação final que ocorre no ponto de salvamento mais externo é o fator determinante em que toda a transação está realmente comprometida com o disco.</span><span class="sxs-lookup"><span data-stu-id="da1f3-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="da1f3-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="da1f3-123">Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="da1f3-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="da1f3-124">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="da1f3-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="da1f3-125">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="da1f3-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="da1f3-126">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="da1f3-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="da1f3-127">Essa opção está disponível em versões do sistema operacional Windows Server a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="da1f3-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="da1f3-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="da1f3-129">Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="da1f3-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="da1f3-130">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="da1f3-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="da1f3-131">Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</span><span class="sxs-lookup"><span data-stu-id="da1f3-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="da1f3-132">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="da1f3-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="da1f3-133">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="da1f3-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da1f3-134">*cmsecDurableCommit*</span><span class="sxs-lookup"><span data-stu-id="da1f3-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="da1f3-135">A duração da confirmação de uma transação lenta.</span><span class="sxs-lookup"><span data-stu-id="da1f3-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="da1f3-136">*pCommitID*</span><span class="sxs-lookup"><span data-stu-id="da1f3-136">*pCommitID*</span></span>

<span data-ttu-id="da1f3-137">A ID de confirmação associada a este registro de confirmação.</span><span class="sxs-lookup"><span data-stu-id="da1f3-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="da1f3-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da1f3-138">Return value</span></span>

<span data-ttu-id="da1f3-139">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da1f3-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="da1f3-140">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="da1f3-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da1f3-141">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="da1f3-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="da1f3-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="da1f3-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="da1f3-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="da1f3-144">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="da1f3-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="da1f3-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="da1f3-146">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="da1f3-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="da1f3-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="da1f3-148">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="da1f3-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="da1f3-149">Esse erro só será retornado pelas versões do sistema operacional Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da1f3-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="da1f3-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="da1f3-151">Uma das opções solicitadas era inválida ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="da1f3-152">Esse erro será retornado pela função <strong>JetCommitTransaction2</strong> quando ocorrer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="da1f3-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="da1f3-153">Um <em>grbit</em> inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="da1f3-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="da1f3-154">JET_bitWaitLastLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="da1f3-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="da1f3-155">JET_bitWaitAllLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="da1f3-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="da1f3-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="da1f3-157">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="da1f3-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="da1f3-159">A operação falhou porque a sessão especificada não está em uma transação.</span><span class="sxs-lookup"><span data-stu-id="da1f3-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="da1f3-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="da1f3-161">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="da1f3-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="da1f3-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="da1f3-163">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="da1f3-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="da1f3-164">Esse erro só será retornado pelas versões do sistema operacional Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da1f3-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="da1f3-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="da1f3-166">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="da1f3-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da1f3-167">Em caso de sucesso, as alterações feitas no banco de dados durante o ponto de salvamento atual para a sessão especificada serão confirmadas e o ponto de salvamento será encerrado.</span><span class="sxs-lookup"><span data-stu-id="da1f3-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="da1f3-168">Se o último ponto de salvamento da sessão for encerrado, a transação será, opcionalmente, liberada para o arquivo de log de transações e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="da1f3-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="da1f3-169">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="da1f3-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="da1f3-170">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="da1f3-170">No change to the database state will occur.</span></span> <span data-ttu-id="da1f3-171">O aplicativo deve chamar a função [JetRollback](./jetrollback-function.md) para anular a transação.</span><span class="sxs-lookup"><span data-stu-id="da1f3-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="da1f3-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="da1f3-172">Remarks</span></span>

<span data-ttu-id="da1f3-173">Deve haver uma chamada para **JetCommitTransaction2** ou [JetRollback](./jetrollback-function.md) para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.</span><span class="sxs-lookup"><span data-stu-id="da1f3-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="da1f3-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1f3-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-175"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="da1f3-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da1f3-176">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da1f3-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-177"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="da1f3-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da1f3-178">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="da1f3-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-179"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="da1f3-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da1f3-180">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="da1f3-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da1f3-181"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="da1f3-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="da1f3-182">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="da1f3-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da1f3-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="da1f3-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="da1f3-184">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="da1f3-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="da1f3-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="da1f3-185">See also</span></span>

[<span data-ttu-id="da1f3-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="da1f3-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="da1f3-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="da1f3-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="da1f3-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="da1f3-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="da1f3-189">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="da1f3-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="da1f3-190">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="da1f3-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="da1f3-191">JetRollback</span><span class="sxs-lookup"><span data-stu-id="da1f3-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="da1f3-192">JetStopService</span><span class="sxs-lookup"><span data-stu-id="da1f3-192">JetStopService</span></span>](./jetstopservice-function.md)
