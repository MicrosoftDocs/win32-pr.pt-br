---
description: 'Saiba mais sobre: função JetPrepareUpdate'
title: Função JetPrepareUpdate
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748666"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="6f0d8-103">Função JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="6f0d8-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="6f0d8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6f0d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="6f0d8-105">Função JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="6f0d8-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="6f0d8-106">A função **JetPrepareUpdate** é a primeira operação na execução de uma atualização, para a inserção de um novo registro ou a substituição de um registro existente por novos valores.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="6f0d8-107">As atualizações são feitas chamando **JetPrepareUpdate**, depois chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) zero ou mais vezes e finalmente chamando [JetUpdate](./jetupdate-function.md) para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="6f0d8-108">**JetPrepareUpdate** e [JetUpdate](./jetupdate-function.md) definem os limites para uma operação de atualização e são importantes para ter apenas o estado de atualização final de um registro inserido em índices.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="6f0d8-109">Isso é mais eficiente, mas também necessário nos casos em que os dados devem corresponder a um estado válido através de mais de uma operação de definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="6f0d8-110">Há algumas opções diferentes para inserir ou substituir registros e eles são descritos mais detalhadamente abaixo.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="6f0d8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f0d8-111">Parameters</span></span>

<span data-ttu-id="6f0d8-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6f0d8-112">*sesid*</span></span>

<span data-ttu-id="6f0d8-113">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-113">The session to use for this call.</span></span>

<span data-ttu-id="6f0d8-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="6f0d8-114">*tableid*</span></span>

<span data-ttu-id="6f0d8-115">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-115">The cursor to use for this call.</span></span>

<span data-ttu-id="6f0d8-116">*Prep*</span><span class="sxs-lookup"><span data-stu-id="6f0d8-116">*prep*</span></span>

<span data-ttu-id="6f0d8-117">As opções que podem ser usadas para se preparar para uma atualização, que incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0d8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6f0d8-118">Value</span></span></p></th>
<th><p><span data-ttu-id="6f0d8-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6f0d8-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="6f0d8-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-121">Esse sinalizador faz com que <strong>JetPrepareUpdate</strong> cancele a atualização para este cursor.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="6f0d8-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-123">Esse sinalizador faz com que o cursor se prepare para uma inserção de um novo registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="6f0d8-124">Todos os dados são inicializados para o estado padrão do registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="6f0d8-125">Se a tabela tiver uma coluna de incremento automático, um novo valor será atribuído a esse registro, independentemente de a atualização ter êxito ou não ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="6f0d8-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-127">Esse sinalizador faz com que o cursor se prepare para uma inserção de uma cópia do registro existente.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="6f0d8-128">Deve haver um registro atual se essa opção for usada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="6f0d8-129">O estado inicial do novo registro é copiado do registro atual.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="6f0d8-130">Valores longos armazenados fora do registro são praticamente copiados.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="6f0d8-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-132">Esse sinalizador faz com que o cursor se prepare para uma inserção do mesmo registro e um Delete ou o registro original.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="6f0d8-133">Ele é usado em casos em que a chave primária foi alterada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="6f0d8-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-135">Esse sinalizador faz com que o cursor se prepare para uma substituição do registro atual.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="6f0d8-136">Se a tabela tiver uma coluna de versão, a coluna versão será definida como o próximo valor em sua sequência.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="6f0d8-137">Se essa atualização não for concluída, o valor da versão no registro não será afetado.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="6f0d8-138">Um bloqueio de atualização é obtido no registro para impedir que outras sessões atualizem esse registro antes da conclusão desta sessão.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="6f0d8-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-140">Esse sinalizador é semelhante a JET_prepReplace, mas nenhum bloqueio é usado para impedir que outras sessões atualizem esse registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="6f0d8-141">Em vez disso, essa sessão pode receber JET_errWriteConflict quando chama <a href="gg269288(v=exchg.10).md">JetUpdate</a> para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6f0d8-142">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6f0d8-142">Return Value</span></span>

<span data-ttu-id="6f0d8-143">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6f0d8-144">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6f0d8-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0d8-145">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6f0d8-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="6f0d8-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f0d8-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6f0d8-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-148">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="6f0d8-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-150"><strong>JetPrepareUpdate</strong> foi chamado com um sinalizador válido para Prep, mas não JET_prepCancel e o cursor já estava no estado preparado.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6f0d8-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-152">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6f0d8-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-154">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6f0d8-155">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6f0d8-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-157">O sinalizador de preparação fornecido não é um sinalizador válido.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6f0d8-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-159">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="6f0d8-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-161"><strong>JetPrepareUpdate</strong> foi chamado para substituir um registro que tinha colunas SLV.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="6f0d8-162">Colunas SLV.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-162">SLV columns.</span></span> <span data-ttu-id="6f0d8-163">Observe que as colunas SLV são um recurso não destinado ao uso geral.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="6f0d8-164">Esse recurso é usado para dar suporte à infraestrutura do Microsoft Exchange e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6f0d8-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-166">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="6f0d8-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-168"><strong>JetPrepareUpdate</strong> foi chamado com JET_prepCancel, mas não pôde reverter todas as alterações feitas em colunas do tipo JET_coltypLongText e/ou colunas do tipo JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6f0d8-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-170">Esse sinalizador não pode ser usado com a mesma sessão de mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="6f0d8-171">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6f0d8-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-173">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="6f0d8-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="6f0d8-175"><strong>JetPrepareUpdate</strong> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f0d8-176">Em caso de sucesso, o cursor é alterado para o estado preparado para a finalidade da atualização desejada ou, no caso de JET_prepCancel, o cursor é revertido para o estado não preparado e todas as alterações são descartadas.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="6f0d8-177">Em caso de falha, o estado do cursor permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="6f0d8-178">Se a falha foi JET_errRollbackError, o estado do cursor será alterado para o estado não preparado, mas nem todas as alterações serão revertidas.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6f0d8-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f0d8-179">Remarks</span></span>

<span data-ttu-id="6f0d8-180">A inserção de uma cópia de um registro é uma otimização importante quando os registros compartilham dados do tipo JET_coltypLongText e/ou JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="6f0d8-181">Esses dados são armazenados fora do registro quando for grande e é possível que vários registros compartilhem a mesma representação física dos dados.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="6f0d8-182">Nesse caso, os dados podem ser atualizados a partir de um dos registros, mas fazer isso fará com que os dados sejam intermitentes, de modo que cada registro tenha sua própria cópia.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="6f0d8-183">Não é possível alterar dados em um registro por uma modificação de outro registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="6f0d8-184">Além disso, não é possível bloquear uma atualização de um registro por uma atualização de outro registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="6f0d8-185">Esse é um recurso central para o ESE e é conhecido como bloqueio no nível de registro.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="6f0d8-186">Operações [JetUpdate](./jetupdate-function.md) que falham deixam o cursor no estado pronto para atualização.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="6f0d8-187">Isso é para permitir a correção para alguns erros, como um valor de coluna errado, sem exigir que o estado de atualização seja recriado.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="6f0d8-188">Isso significa que, em todos os casos em que um cursor abandona uma atualização, ele deve chamar **JetPrepareUpdate** explicitamente com JET_prepCancel.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6f0d8-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f0d8-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-190"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6f0d8-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0d8-191">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-192"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6f0d8-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0d8-193">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-194"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6f0d8-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0d8-195">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0d8-196"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6f0d8-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0d8-197">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0d8-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6f0d8-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0d8-199">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6f0d8-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6f0d8-200">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6f0d8-200">See Also</span></span>

[<span data-ttu-id="6f0d8-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6f0d8-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6f0d8-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6f0d8-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6f0d8-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6f0d8-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6f0d8-204">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="6f0d8-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="6f0d8-205">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="6f0d8-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="6f0d8-206">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="6f0d8-206">JetUpdate</span></span>](./jetupdate-function.md)
