---
description: 'Saiba mais sobre: função JetGetLock'
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
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104092013"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="fd5b5-103">Função JetGetLock</span><span class="sxs-lookup"><span data-stu-id="fd5b5-103">JetGetLock Function</span></span>


<span data-ttu-id="fd5b5-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fd5b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="fd5b5-105">Função JetGetLock</span><span class="sxs-lookup"><span data-stu-id="fd5b5-105">JetGetLock Function</span></span>

<span data-ttu-id="fd5b5-106">A função **JetGetLock** fornece um meio para reservar explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="fd5b5-107">Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="fd5b5-108">Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="fd5b5-109">No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização, ou para garantir que uma operação subsequente terá sucesso em virtude de que os bloqueios necessários já foram feitos.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="fd5b5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd5b5-110">Parameters</span></span>

<span data-ttu-id="fd5b5-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fd5b5-111">*sesid*</span></span>

<span data-ttu-id="fd5b5-112">A sessão que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-112">The session that will be used for this call.</span></span>

<span data-ttu-id="fd5b5-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="fd5b5-113">*tableid*</span></span>

<span data-ttu-id="fd5b5-114">O cursor que será usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="fd5b5-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fd5b5-115">*grbit*</span></span>

<span data-ttu-id="fd5b5-116">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="fd5b5-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd5b5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fd5b5-117">Value</span></span></p></th>
<th><p><span data-ttu-id="fd5b5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fd5b5-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="fd5b5-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-120">Esse sinalizador faz com que um bloqueio de leitura seja adquirido no registro atual.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="fd5b5-121">Os bloqueios de leitura são incompatíveis com os bloqueios de gravação já mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos por outras sessões.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="fd5b5-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-123">Esse sinalizador faz com que um bloqueio de gravação seja adquirido no registro atual.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="fd5b5-124">Os bloqueios de gravação não são compatíveis com bloqueios de gravação ou leitura mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos pela mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fd5b5-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fd5b5-125">Return Value</span></span>

<span data-ttu-id="fd5b5-126">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fd5b5-127">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fd5b5-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd5b5-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fd5b5-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="fd5b5-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd5b5-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fd5b5-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-131">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fd5b5-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-133">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fd5b5-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-135">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fd5b5-136">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="fd5b5-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-138">O <em>grbit</em> fornecido não é JET_bitReadLock ou JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="fd5b5-139">Ele deve ser um desses dois sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="fd5b5-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-141">O cursor deve estar em um registro para adquirir um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="fd5b5-142">Os bloqueios estão sempre em registros.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fd5b5-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-144">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="fd5b5-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-146">Os bloqueios só podem ser adquiridos por sessões em uma transação.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="fd5b5-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-148">O cursor não pode ser somente leitura e adquirir um bloqueio de gravação.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fd5b5-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-150">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fd5b5-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-152">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="fd5b5-153">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fd5b5-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-155">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="fd5b5-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-157">A sessão deve ter permissões de gravação para adquirir o bloqueio de gravação.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="fd5b5-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="fd5b5-159">O erro retornado quando um bloqueio conflitante é solicitado.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd5b5-160">Em caso de sucesso, a sessão adquiriu o bloqueio solicitado.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="fd5b5-161">Em caso de falha, a sessão não adquiriu o bloqueio solicitado.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fd5b5-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd5b5-162">Remarks</span></span>

<span data-ttu-id="fd5b5-163">Os bloqueios de gravação não podem ser adquiridos com sessões ou cursores que têm permissões somente leitura, mesmo que a sessão e o cursor, em última instância, não executem uma operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="fd5b5-164">Tanto a sessão quanto o cursor devem ter privilégios de gravação para adquirir um bloqueio de gravação.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="fd5b5-165">Bloqueios de leitura e gravação são um meio de bloqueio pessimista.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="fd5b5-166">O bloqueio pessimista espera que várias sessões simultâneas entrem em conflito e adquiram bloqueios antecipadamente para garantir que suas operações tenham sucesso.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="fd5b5-167">A maioria das operações será serializável em virtude de bloqueios implicitamente feitos.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="fd5b5-168">No entanto, algumas operações não serão.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-168">However, some operations will not.</span></span> <span data-ttu-id="fd5b5-169">Para ilustrar isso, considere as duas transações,</span><span class="sxs-lookup"><span data-stu-id="fd5b5-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="fd5b5-170">T1: R (A), U (B)</span><span class="sxs-lookup"><span data-stu-id="fd5b5-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="fd5b5-171">T2: R (B), U (A)</span><span class="sxs-lookup"><span data-stu-id="fd5b5-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="fd5b5-172">O controle de versão em nível de registro garantirá que cada transação, quando executada simultaneamente, verá os valores originais para A e B. Não há nenhuma ordem de série de execução que possa produzir os mesmos resultados para A e B no caso de os resultados dependerem dos dados lidos.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="fd5b5-173">Para que o aplicativo faça essa transação serializável, ele deve adquirir um bloqueio de leitura explícito em A e B em cada transação quando o valor for lido.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fd5b5-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd5b5-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-175"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fd5b5-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fd5b5-176">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-177"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="fd5b5-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fd5b5-178">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-179"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="fd5b5-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fd5b5-180">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd5b5-181"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="fd5b5-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fd5b5-182">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd5b5-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fd5b5-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fd5b5-184">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fd5b5-185">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fd5b5-185">See Also</span></span>

[<span data-ttu-id="fd5b5-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fd5b5-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fd5b5-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fd5b5-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fd5b5-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fd5b5-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fd5b5-189">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="fd5b5-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="fd5b5-190">JetStopService</span><span class="sxs-lookup"><span data-stu-id="fd5b5-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="fd5b5-191">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="fd5b5-191">JetUpdate</span></span>](./jetupdate-function.md)
