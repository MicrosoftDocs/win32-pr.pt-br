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
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802074"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="98758-103">Função JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="98758-103">JetDupCursor Function</span></span>


<span data-ttu-id="98758-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98758-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="98758-105">Função JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="98758-105">JetDupCursor Function</span></span>

<span data-ttu-id="98758-106">A função **JetDupCursor** duplica um cursor Open e retorna um identificador para o cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="98758-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="98758-107">Se o cursor que foi duplicado era um cursor somente leitura, o cursor duplicado também é um cursor somente leitura.</span><span class="sxs-lookup"><span data-stu-id="98758-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="98758-108">Qualquer estado relacionado à construção de uma chave de pesquisa ou à atualização de um registro não é copiado para o cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="98758-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="98758-109">Além disso, o local do cursor original não é duplicado no cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="98758-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="98758-110">O cursor duplicado sempre é aberto no índice clusterizado e seu local está sempre na primeira linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="98758-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="98758-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98758-111">Parameters</span></span>

<span data-ttu-id="98758-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="98758-112">*sesid*</span></span>

<span data-ttu-id="98758-113">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="98758-113">The session to use for this call.</span></span>

<span data-ttu-id="98758-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="98758-114">*tableid*</span></span>

<span data-ttu-id="98758-115">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="98758-115">The cursor to use for this call.</span></span>

<span data-ttu-id="98758-116">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="98758-116">*ptableid*</span></span>

<span data-ttu-id="98758-117">Ponteiro para *TableName*.</span><span class="sxs-lookup"><span data-stu-id="98758-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="98758-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="98758-118">*grbit*</span></span>

<span data-ttu-id="98758-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="98758-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="98758-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="98758-120">Return Value</span></span>

<span data-ttu-id="98758-121">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="98758-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98758-122">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98758-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98758-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="98758-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="98758-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="98758-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98758-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98758-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98758-126">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="98758-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98758-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98758-128">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="98758-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98758-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98758-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98758-130">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="98758-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="98758-131">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="98758-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98758-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98758-133">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="98758-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98758-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="98758-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="98758-135">Não existem recursos de cursor disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98758-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98758-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98758-137">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="98758-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98758-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="98758-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="98758-139">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="98758-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="98758-140">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="98758-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98758-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98758-142">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="98758-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98758-143">Em caso de sucesso, *pTableID* é definido como um cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="98758-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="98758-144">Em caso de falha, nenhuma alteração é feita.</span><span class="sxs-lookup"><span data-stu-id="98758-144">On failure, no changes are made.</span></span> <span data-ttu-id="98758-145">O estado de *TableName* não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="98758-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98758-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="98758-146">Remarks</span></span>

<span data-ttu-id="98758-147">O cursor duplicado não tem o estado do cursor inteiro copiado.</span><span class="sxs-lookup"><span data-stu-id="98758-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="98758-148">O local do cursor duplicado, incluindo o índice atual, geralmente é diferente do cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="98758-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="98758-149">O cursor duplicado sempre é retornado no índice clusterizado e na primeira linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="98758-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="98758-150">Se a tabela estiver vazia, o cursor duplicado não estará em nenhuma linha.</span><span class="sxs-lookup"><span data-stu-id="98758-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="98758-151">As tabelas abertas com **JetDupCursor** normalmente devem ser fechadas com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="98758-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="98758-152">A exceção a essa regra ocorre quando **JetDupCursor** é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="98758-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="98758-153">Ao reverter uma transação, o cursor é fechado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="98758-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="98758-154">Nesse caso, é um erro fechar a tabela com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="98758-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="98758-155">O número de tabelas que podem ser abertas simultaneamente é afetado diretamente pelo [JET_paramMaxOpenTables](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98758-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="98758-156">Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="98758-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98758-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98758-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98758-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="98758-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98758-159">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98758-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-160"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="98758-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98758-161">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98758-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98758-162"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="98758-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98758-163">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="98758-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98758-164"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="98758-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98758-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98758-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98758-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98758-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98758-167">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98758-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98758-168">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="98758-168">See Also</span></span>

[<span data-ttu-id="98758-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="98758-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="98758-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="98758-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="98758-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="98758-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="98758-172">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="98758-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="98758-173">JetRollback</span><span class="sxs-lookup"><span data-stu-id="98758-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="98758-174">JetStopService</span><span class="sxs-lookup"><span data-stu-id="98758-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="98758-175">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="98758-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
