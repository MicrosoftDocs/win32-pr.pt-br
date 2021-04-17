---
description: 'Saiba mais sobre: função JetEscrowUpdate'
title: Função JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797982"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="4e756-103">Função JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4e756-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="4e756-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4e756-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="4e756-105">Função JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4e756-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="4e756-106">A função **JetEscrowUpdate** executa uma operação de adição atômica em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="4e756-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="4e756-107">Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="4e756-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4e756-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e756-108">Parameters</span></span>

<span data-ttu-id="4e756-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4e756-109">*sesid*</span></span>

<span data-ttu-id="4e756-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="4e756-110">The session to use for this call.</span></span>

<span data-ttu-id="4e756-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4e756-111">*tableid*</span></span>

<span data-ttu-id="4e756-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="4e756-112">The cursor to use for this call.</span></span>

<span data-ttu-id="4e756-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="4e756-113">*columnid*</span></span>

<span data-ttu-id="4e756-114">O *columnid* da coluna a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4e756-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="4e756-115">*PV*</span><span class="sxs-lookup"><span data-stu-id="4e756-115">*pv*</span></span>

<span data-ttu-id="4e756-116">Um ponteiro para um buffer que contém o adendo para a coluna.</span><span class="sxs-lookup"><span data-stu-id="4e756-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="4e756-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="4e756-117">*cbMax*</span></span>

<span data-ttu-id="4e756-118">O tamanho do buffer que contém o adendo.</span><span class="sxs-lookup"><span data-stu-id="4e756-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="4e756-119">*pvOld*</span><span class="sxs-lookup"><span data-stu-id="4e756-119">*pvOld*</span></span>

<span data-ttu-id="4e756-120">O buffer de saída que receberá o valor atual da coluna como armazenado no banco de dados (o controle de versão é ignorado).</span><span class="sxs-lookup"><span data-stu-id="4e756-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="4e756-121">*cbOldMax*</span><span class="sxs-lookup"><span data-stu-id="4e756-121">*cbOldMax*</span></span>

<span data-ttu-id="4e756-122">O tamanho máximo do buffer de saída que receberá o valor atual da coluna.</span><span class="sxs-lookup"><span data-stu-id="4e756-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="4e756-123">Atualmente, apenas JET_coltypLong tem suporte, portanto, o buffer deve ter 4 bytes ou 0 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="4e756-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="4e756-124">Se *pvOld* for NULL, *cbOldMax* deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="4e756-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="4e756-125">*pcbOldActual*</span><span class="sxs-lookup"><span data-stu-id="4e756-125">*pcbOldActual*</span></span>

<span data-ttu-id="4e756-126">Recebe a quantidade real de dados de valor bruto recebidos no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4e756-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="4e756-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4e756-127">*grbit*</span></span>

<span data-ttu-id="4e756-128">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e756-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e756-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4e756-129">Value</span></span></p></th>
<th><p><span data-ttu-id="4e756-130">Significado</span><span class="sxs-lookup"><span data-stu-id="4e756-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e756-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="4e756-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="4e756-132">Mesmo que a sessão que executa a atualização de caução tenha sua reversão de transação, essa atualização não será desfeita.</span><span class="sxs-lookup"><span data-stu-id="4e756-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="4e756-133">Observe que, como os registros de log podem não ser liberados para o disco, as atualizações de caução recentes feitas com esse sinalizador poderão ser perdidas se houver uma falha.</span><span class="sxs-lookup"><span data-stu-id="4e756-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4e756-134">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4e756-134">Return Value</span></span>

<span data-ttu-id="4e756-135">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e756-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4e756-136">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4e756-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e756-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4e756-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="4e756-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e756-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e756-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4e756-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4e756-140">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4e756-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="4e756-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="4e756-142">O cursor tem uma atualização preparada com <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="4e756-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4e756-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4e756-144">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4e756-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4e756-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4e756-146">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="4e756-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4e756-147">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="4e756-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="4e756-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="4e756-149">Um tamanho de buffer inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="4e756-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="4e756-150">Atualmente, apenas JET_coltypLong tem suporte, portanto, o buffer deve ter 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4e756-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="4e756-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="4e756-152">Uma coluna inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="4e756-152">An invalid column has been specified.</span></span> <span data-ttu-id="4e756-153">A coluna deve ser criada com JET_bitColumnEscrowUpdate especificado.</span><span class="sxs-lookup"><span data-stu-id="4e756-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="4e756-154">Somente colunas fixas de JET_coltypLong podem ser especificadas como de caução atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="4e756-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4e756-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4e756-156">O cursor deve estar em um registro para atualizar uma coluna.</span><span class="sxs-lookup"><span data-stu-id="4e756-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="4e756-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="4e756-158">As atualizações de caução só podem ser executadas por sessões em uma transação.</span><span class="sxs-lookup"><span data-stu-id="4e756-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4e756-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4e756-160">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="4e756-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="4e756-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="4e756-162">O cursor não pode ser somente leitura e atualizar um registro.</span><span class="sxs-lookup"><span data-stu-id="4e756-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4e756-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4e756-164">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="4e756-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4e756-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4e756-166">A mesma sessão não pode ser usada em mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="4e756-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="4e756-167">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="4e756-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4e756-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4e756-169">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="4e756-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="4e756-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4e756-171">A sessão deve ter permissões de gravação para atualizar um registro.</span><span class="sxs-lookup"><span data-stu-id="4e756-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-173">O erro retornado quando uma atualização conflitante é solicitada.</span><span class="sxs-lookup"><span data-stu-id="4e756-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4e756-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e756-174">Remarks</span></span>

<span data-ttu-id="4e756-175">Normalmente, se duas sessões tentarem atualizar um registro simultaneamente, a segunda sessão receberá um erro de JET_errWriteConflict, a menos que as sessões sejam completamente serializadas.</span><span class="sxs-lookup"><span data-stu-id="4e756-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="4e756-176">Para serializar duas sessões que atualizam o mesmo registro, a segunda sessão deve iniciar sua transação após a primeira transação confirmar sua transação.</span><span class="sxs-lookup"><span data-stu-id="4e756-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="4e756-177">Consulte [JetBeginTransaction](./jetbegintransaction-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4e756-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="4e756-178">Várias colunas no mesmo registro podem ser atualizadas por caução.</span><span class="sxs-lookup"><span data-stu-id="4e756-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="4e756-179">As atualizações não afetam uma à outra.</span><span class="sxs-lookup"><span data-stu-id="4e756-179">The updates do not affect each other.</span></span>

<span data-ttu-id="4e756-180">Somente as operações **JetEscrowUpdate** são compatíveis entre si.</span><span class="sxs-lookup"><span data-stu-id="4e756-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="4e756-181">Se duas sessões diferentes tentarem preparar atualizações ou excluir o mesmo registro, um conflito de gravação será gerado.</span><span class="sxs-lookup"><span data-stu-id="4e756-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="4e756-182">Sessão B</span><span class="sxs-lookup"><span data-stu-id="4e756-182">Session B</span></span><br /><span data-ttu-id="4e756-183">
<strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="4e756-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="4e756-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="4e756-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="4e756-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="4e756-186"><strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4e756-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4e756-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="4e756-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span><span class="sxs-lookup"><span data-stu-id="4e756-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="4e756-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-194">Sessão A</span><span class="sxs-lookup"><span data-stu-id="4e756-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="4e756-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="4e756-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="4e756-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4e756-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4e756-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e756-199">As operações de caução têm controle de versão e são desfeitas usando [JetRollback](./jetrollback-function.md) (a menos que JET_bitEscrowNoRollback tenha sido especificado).</span><span class="sxs-lookup"><span data-stu-id="4e756-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="4e756-200">**JetEscrowUpdate** retorna o valor bruto da coluna armazenada no banco de dados, pois um aplicativo pode querer executar uma ação especial quando um valor de Sentinela é atingido.</span><span class="sxs-lookup"><span data-stu-id="4e756-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="4e756-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) retorna a exibição com controle de versão correta da coluna, ignorando as atualizações feitas por sessões simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4e756-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="4e756-202">Dadas duas sessões operando na mesma coluna do mesmo registro, podemos ver como isso funciona.</span><span class="sxs-lookup"><span data-stu-id="4e756-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="4e756-203">Suponha que a coluna comece com um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="4e756-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e756-204">Session</span><span class="sxs-lookup"><span data-stu-id="4e756-204">Session</span></span></p></th>
<th><p><span data-ttu-id="4e756-205">Operação</span><span class="sxs-lookup"><span data-stu-id="4e756-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="4e756-206">Valor armazenado</span><span class="sxs-lookup"><span data-stu-id="4e756-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="4e756-207">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4e756-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e756-208">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-208">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="4e756-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-210">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-210">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="4e756-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-212">0</span><span class="sxs-lookup"><span data-stu-id="4e756-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-213">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-213">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-214"><strong>JetEscrowUpdate</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="4e756-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="4e756-215">4</span><span class="sxs-lookup"><span data-stu-id="4e756-215">4</span></span></p></td>
<td><p><span data-ttu-id="4e756-216">0</span><span class="sxs-lookup"><span data-stu-id="4e756-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-217">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-217">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-219">4</span><span class="sxs-lookup"><span data-stu-id="4e756-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-220">B</span><span class="sxs-lookup"><span data-stu-id="4e756-220">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="4e756-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-222">B</span><span class="sxs-lookup"><span data-stu-id="4e756-222">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-224">0</span><span class="sxs-lookup"><span data-stu-id="4e756-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-225">B</span><span class="sxs-lookup"><span data-stu-id="4e756-225">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-226"><strong>JetEscrowUpdate</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="4e756-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="4e756-227">7</span><span class="sxs-lookup"><span data-stu-id="4e756-227">7</span></span></p></td>
<td><p><span data-ttu-id="4e756-228">4</span><span class="sxs-lookup"><span data-stu-id="4e756-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-229">B</span><span class="sxs-lookup"><span data-stu-id="4e756-229">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-231">3</span><span class="sxs-lookup"><span data-stu-id="4e756-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-232">A</span><span class="sxs-lookup"><span data-stu-id="4e756-232">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-233"><strong>JetEscrowUpdate</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="4e756-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="4e756-234">9</span><span class="sxs-lookup"><span data-stu-id="4e756-234">9</span></span></p></td>
<td><p><span data-ttu-id="4e756-235">7</span><span class="sxs-lookup"><span data-stu-id="4e756-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-236">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-236">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-237"><strong>JetEscrowUpdate</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="4e756-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="4e756-238">2</span><span class="sxs-lookup"><span data-stu-id="4e756-238">2</span></span></p></td>
<td><p><span data-ttu-id="4e756-239">9</span><span class="sxs-lookup"><span data-stu-id="4e756-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-240">B</span><span class="sxs-lookup"><span data-stu-id="4e756-240">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-242">3</span><span class="sxs-lookup"><span data-stu-id="4e756-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-243">A</span><span class="sxs-lookup"><span data-stu-id="4e756-243">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-245">-1</span><span class="sxs-lookup"><span data-stu-id="4e756-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-246">B</span><span class="sxs-lookup"><span data-stu-id="4e756-246">B</span></span></p></td>
<td><p><span data-ttu-id="4e756-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="4e756-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="4e756-248">-1</span><span class="sxs-lookup"><span data-stu-id="4e756-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-249">Um</span><span class="sxs-lookup"><span data-stu-id="4e756-249">A</span></span></p></td>
<td><p><span data-ttu-id="4e756-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="4e756-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4e756-251">-1</span><span class="sxs-lookup"><span data-stu-id="4e756-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e756-252">Não é recomendável substituir um registro na mesma transação que executa atualizações de caução em um registro.</span><span class="sxs-lookup"><span data-stu-id="4e756-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="4e756-253">Em particular, se uma atualização em um registro estiver preparada com uma [JET_TABLEID](./jet-tableid.md) e uma [JET_TABLEID](./jet-tableid.md) diferente for usada para atualizar o registro, a caução atualizada será perdida quando [JetUpdate](./jetupdate-function.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="4e756-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="4e756-254">Isso acontece mesmo que a coluna de caução não tenha sido definida durante a atualização.</span><span class="sxs-lookup"><span data-stu-id="4e756-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="4e756-255">Quando uma coluna atualizável de caução tem um valor igual a zero, o comportamento especial pode ser disparado.</span><span class="sxs-lookup"><span data-stu-id="4e756-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="4e756-256">Esse comportamento ocorre apenas se uma operação **JetEscrowUpdate** faz com que a coluna tenha um valor igual a zero.</span><span class="sxs-lookup"><span data-stu-id="4e756-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="4e756-257">A ação não acontece imediatamente, mas ocorre em algum momento após a transação que fez com que a coluna tenha um valor de zero confirmações.</span><span class="sxs-lookup"><span data-stu-id="4e756-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="4e756-258">A coluna ainda deve ter um valor igual a zero (ou seja, se nenhuma outra sessão tiver modificado a coluna).</span><span class="sxs-lookup"><span data-stu-id="4e756-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="4e756-259">Se a coluna tiver sido criada com JET_bitColumnDeleteOnZero, o registro que contém a coluna será excluído.</span><span class="sxs-lookup"><span data-stu-id="4e756-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="4e756-260">Se a coluna tiver sido criada com JET_bitColumnFinalize, um retorno de chamada será emitido.</span><span class="sxs-lookup"><span data-stu-id="4e756-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="4e756-261">Uma falha pode fazer com que essas ações não aconteçam, mas a manutenção online (usando a função [JetDefragment](./jetdefragment-function.md) ) fará com que as ações sejam refeitas corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e756-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4e756-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e756-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e756-263"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-264">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4e756-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-265"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-266">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4e756-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-267"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-268">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4e756-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e756-269"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-270">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4e756-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e756-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4e756-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4e756-272">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4e756-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4e756-273">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4e756-273">See Also</span></span>

[<span data-ttu-id="4e756-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4e756-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4e756-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4e756-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4e756-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4e756-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4e756-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4e756-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4e756-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4e756-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4e756-279">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="4e756-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="4e756-280">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="4e756-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="4e756-281">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="4e756-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="4e756-282">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="4e756-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="4e756-283">JetRollback</span><span class="sxs-lookup"><span data-stu-id="4e756-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="4e756-284">JetStopService</span><span class="sxs-lookup"><span data-stu-id="4e756-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="4e756-285">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="4e756-285">JetUpdate</span></span>](./jetupdate-function.md)
