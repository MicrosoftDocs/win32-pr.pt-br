---
description: 'Saiba mais sobre: função JetGetCursorInfo'
title: Função JetGetCursorInfo
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754066"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="20be6-103">Função JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="20be6-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="20be6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20be6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="20be6-105">Função JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="20be6-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="20be6-106">A função **JetGetCursorInfo** é usada para determinar se uma atualização do registro atual de um cursor resultará em um conflito de gravação, com base no status de atualização atual do registro.</span><span class="sxs-lookup"><span data-stu-id="20be6-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="20be6-107">É possível que um conflito de gravação seja retornado, mesmo se **JetGetCursorInfo** retornar JET_errSuccess, porque outra sessão pode atualizar o registro antes que a sessão atual seja capaz de atualizar o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="20be6-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="20be6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20be6-108">Parameters</span></span>

<span data-ttu-id="20be6-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="20be6-109">*sesid*</span></span>

<span data-ttu-id="20be6-110">A sessão que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="20be6-110">The session that will be used for this call.</span></span>

<span data-ttu-id="20be6-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="20be6-111">*tableid*</span></span>

<span data-ttu-id="20be6-112">O cursor que será usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="20be6-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="20be6-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="20be6-113">*pvResult*</span></span>

<span data-ttu-id="20be6-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="20be6-114">Reserved for future use.</span></span>

<span data-ttu-id="20be6-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="20be6-115">*cbMax*</span></span>

<span data-ttu-id="20be6-116">Deve ser definido como 0 (zero), caso contrário, não utilizado.</span><span class="sxs-lookup"><span data-stu-id="20be6-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="20be6-117">Ele está presente para futuras funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="20be6-117">It is present for future functionality.</span></span>

<span data-ttu-id="20be6-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="20be6-118">*InfoLevel*</span></span>

<span data-ttu-id="20be6-119">Deve ser definido como 0 (zero), caso contrário, não utilizado.</span><span class="sxs-lookup"><span data-stu-id="20be6-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="20be6-120">Ele está presente para futuras funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="20be6-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="20be6-121">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="20be6-121">Return Value</span></span>

<span data-ttu-id="20be6-122">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="20be6-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20be6-123">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="20be6-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20be6-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="20be6-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="20be6-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="20be6-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20be6-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20be6-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20be6-127">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="20be6-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="20be6-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="20be6-129">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="20be6-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="20be6-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="20be6-131">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="20be6-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="20be6-132">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="20be6-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="20be6-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="20be6-134">O <em>cbMax</em> não é 0 (zero) ou <em>InfoLevel</em> não é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="20be6-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="20be6-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="20be6-136">O cursor não está atualmente em um registro e as informações em um registro lógico não podem ser retornadas como resultado.</span><span class="sxs-lookup"><span data-stu-id="20be6-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="20be6-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="20be6-138">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="20be6-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="20be6-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="20be6-140">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="20be6-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="20be6-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="20be6-142">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="20be6-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="20be6-143">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="20be6-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="20be6-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="20be6-145">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="20be6-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="20be6-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="20be6-147">O registro atual do cursor foi atualizado por outra sessão e uma atualização desse registro por esta sessão resultará em um conflito de gravação.</span><span class="sxs-lookup"><span data-stu-id="20be6-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20be6-148">Em caso de sucesso, essa operação não tem efeito sobre o local do cursor, mas indica apenas que nenhuma outra sessão atualizou esse registro no momento.</span><span class="sxs-lookup"><span data-stu-id="20be6-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="20be6-149">Em caso de falha, se um código de erro negativo for retornado, não haverá efeitos para o cursor ou o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="20be6-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20be6-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="20be6-150">Remarks</span></span>

<span data-ttu-id="20be6-151">Esta operação não afeta o estado do cursor ou dos dados.</span><span class="sxs-lookup"><span data-stu-id="20be6-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="20be6-152">Ele retorna apenas um código de erro que descreve se uma atualização para o registro atual pela sessão de chamada é conhecida por resultar em um JET_errWriteConflict ou é desconhecido para retornar JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="20be6-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="20be6-153">Se outra sessão já tiver atualizado esse registro para usá-lo, você terá certeza de que uma atualização desse registro por esta sessão resultará em um conflito de gravação.</span><span class="sxs-lookup"><span data-stu-id="20be6-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="20be6-154">Isso será verdadeiro até que esta sessão confirme ou reverta suas transações para o nível de transação 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="20be6-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="20be6-155">No entanto, se **JetGetCursorInfo** retornar JET_errSuccess, ainda é possível que outra sessão atualize esse registro antes da sessão atual e, portanto, ainda é possível que uma atualização do registro atual por essa sessão em sua transação atual resulte em um conflito de gravação.</span><span class="sxs-lookup"><span data-stu-id="20be6-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="20be6-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20be6-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20be6-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="20be6-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20be6-158">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20be6-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-159"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="20be6-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20be6-160">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20be6-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-161"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="20be6-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20be6-162">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="20be6-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20be6-163"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="20be6-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20be6-164">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20be6-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20be6-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="20be6-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20be6-166">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20be6-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20be6-167">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="20be6-167">See Also</span></span>

[<span data-ttu-id="20be6-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20be6-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20be6-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20be6-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20be6-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="20be6-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="20be6-171">JetGetLock</span><span class="sxs-lookup"><span data-stu-id="20be6-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="20be6-172">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="20be6-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="20be6-173">JetStopService</span><span class="sxs-lookup"><span data-stu-id="20be6-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="20be6-174">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="20be6-174">JetUpdate</span></span>](./jetupdate-function.md)
