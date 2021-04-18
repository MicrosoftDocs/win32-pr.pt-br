---
description: 'Saiba mais sobre: função JetDelete'
title: Função JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752328"
---
# <a name="jetdelete-function"></a><span data-ttu-id="8a637-103">Função JetDelete</span><span class="sxs-lookup"><span data-stu-id="8a637-103">JetDelete Function</span></span>


<span data-ttu-id="8a637-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8a637-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="8a637-105">Função JetDelete</span><span class="sxs-lookup"><span data-stu-id="8a637-105">JetDelete Function</span></span>

<span data-ttu-id="8a637-106">A função **JetDelete** exclui o registro atual em uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8a637-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="8a637-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a637-107">Parameters</span></span>

<span data-ttu-id="8a637-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8a637-108">*sesid*</span></span>

<span data-ttu-id="8a637-109">O contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="8a637-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="8a637-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8a637-110">*tableid*</span></span>

<span data-ttu-id="8a637-111">O cursor em uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8a637-111">The cursor on a database table.</span></span> <span data-ttu-id="8a637-112">A linha atual será excluída.</span><span class="sxs-lookup"><span data-stu-id="8a637-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="8a637-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8a637-113">Return Value</span></span>

<span data-ttu-id="8a637-114">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a637-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8a637-115">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8a637-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a637-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a637-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="8a637-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a637-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a637-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8a637-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8a637-119">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8a637-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="8a637-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="8a637-121">A função de retorno de chamada falhou de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="8a637-121">The callback function failed in some manner.</span></span> <span data-ttu-id="8a637-122">Por exemplo, violações de acesso em funções de retorno de chamada são capturadas e convertidas em JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="8a637-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="8a637-123">Esse erro só será retornado pelo Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="8a637-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8a637-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8a637-125">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8a637-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="8a637-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="8a637-127">O cursor especificado por <em>TableName</em> não oferece suporte à exclusão.</span><span class="sxs-lookup"><span data-stu-id="8a637-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="8a637-128">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="8a637-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8a637-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8a637-130">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="8a637-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8a637-131">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a637-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="8a637-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="8a637-133">O cursor especificado por <em>TableName</em> não está em um registro.</span><span class="sxs-lookup"><span data-stu-id="8a637-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8a637-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8a637-135">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="8a637-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8a637-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8a637-137">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="8a637-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="8a637-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="8a637-139">O mecanismo de banco de dados não tem permissões suficientes para excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="8a637-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="8a637-140">Isso pode acontecer se o arquivo de banco de dados foi aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a637-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="8a637-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="8a637-142">Um buffer de atualização (consulte <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mas nem todas as alterações feitas em colunas do tipo JET_coltypLongText e/ou colunas do tipo JET_coltypLongBinary podem ser revertidas.</span><span class="sxs-lookup"><span data-stu-id="8a637-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8a637-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8a637-144">É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8a637-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="8a637-145">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a637-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8a637-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8a637-147">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="8a637-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="8a637-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="8a637-149">A transação é uma transação somente leitura e não oferece suporte a exclusões.</span><span class="sxs-lookup"><span data-stu-id="8a637-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="8a637-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="8a637-151">A operação falhou porque não há memória suficiente para reter informações transacionais sobre a atualização.</span><span class="sxs-lookup"><span data-stu-id="8a637-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="8a637-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="8a637-153">Outra sessão bloqueou anteriormente o registro para atualização.</span><span class="sxs-lookup"><span data-stu-id="8a637-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="8a637-154">A atualização tentada por esta sessão falhará.</span><span class="sxs-lookup"><span data-stu-id="8a637-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a637-155">Em caso de sucesso, a moeda é deixada logo antes do próximo registro.</span><span class="sxs-lookup"><span data-stu-id="8a637-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="8a637-156">Se o registro excluído foi o último na tabela, a moeda é deixada no final da tabela (ou seja, após o novo último registro).</span><span class="sxs-lookup"><span data-stu-id="8a637-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="8a637-157">Se o registro excluído for o único registro na tabela, a moeda será definida como o início.</span><span class="sxs-lookup"><span data-stu-id="8a637-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="8a637-158">Os índices apropriados são atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8a637-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="8a637-159">Se uma atualização estiver preparada (usando [JetPrepareUpdate](./jetprepareupdate-function.md)), ela será cancelada.</span><span class="sxs-lookup"><span data-stu-id="8a637-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="8a637-160">O buffer de atualização será redefinido.</span><span class="sxs-lookup"><span data-stu-id="8a637-160">The update buffer will be reset.</span></span>

<span data-ttu-id="8a637-161">Em caso de falha, a moeda permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="8a637-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="8a637-162">Se uma atualização estiver preparada (consulte [JetPrepareUpdate](./jetprepareupdate-function.md)), o buffer de atualização poderá ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="8a637-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8a637-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a637-163">Remarks</span></span>

<span data-ttu-id="8a637-164">Nem todas as tabelas dão suporte à exclusão de linhas.</span><span class="sxs-lookup"><span data-stu-id="8a637-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="8a637-165">Normalmente, uma tabela temporária não dá suporte à exclusão de linhas.</span><span class="sxs-lookup"><span data-stu-id="8a637-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="8a637-166">A exclusão de registros pode ser habilitada em tabelas temporárias por vários motivos, algumas das quais são:</span><span class="sxs-lookup"><span data-stu-id="8a637-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="8a637-167">JET_bitTTUpdatable foi especificado durante a criação.</span><span class="sxs-lookup"><span data-stu-id="8a637-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="8a637-168">Tabelas temporárias grandes podem dar suporte à exclusão se elas foram criadas com JET_bitTTScrollable ou JET_bitTTIndexed.</span><span class="sxs-lookup"><span data-stu-id="8a637-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="8a637-169">O limite no qual uma tabela temporária se torna "grande" atualmente é de 64 quilobytes, mas pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="8a637-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="8a637-170">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="8a637-170">Windows XP and later.</span></span> <span data-ttu-id="8a637-171">As funções de retorno de chamada podem ser invocadas por **JetDelete**, incluindo JET_cbtypBeforeDelete e JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="8a637-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="8a637-172">É importante entender o impacto da execução de um grande número de operações de atualização dentro de uma única transação.</span><span class="sxs-lookup"><span data-stu-id="8a637-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="8a637-173">Cada atualização do banco de dados deve ser controlada pelo mecanismo de banco de dados no repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="8a637-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="8a637-174">O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas.</span><span class="sxs-lookup"><span data-stu-id="8a637-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="8a637-175">Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8a637-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="8a637-176">Depois que o mecanismo de banco de dados tiver esgotado os recursos usados para armazenar essas versões, ele não poderá mais aceitar outras alterações até que algumas transações tenham sido concluídas para permitir que esses recursos sejam recuperados.</span><span class="sxs-lookup"><span data-stu-id="8a637-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="8a637-177">Quando o mecanismo estiver nesse estado, todas as atualizações falharão com JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8a637-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="8a637-178">Os recursos disponíveis para o mecanismo de banco de dados para armazenar essas versões podem ser controlados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxVerPages* e *JET_paramGlobalMinVerPages*.</span><span class="sxs-lookup"><span data-stu-id="8a637-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8a637-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a637-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a637-180"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8a637-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a637-181">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8a637-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-182"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8a637-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a637-183">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8a637-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-184"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8a637-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a637-185">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8a637-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a637-186"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="8a637-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8a637-187">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8a637-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a637-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8a637-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8a637-189">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8a637-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8a637-190">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8a637-190">See Also</span></span>

[<span data-ttu-id="8a637-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8a637-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8a637-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8a637-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8a637-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8a637-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8a637-194">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="8a637-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="8a637-195">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="8a637-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="8a637-196">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="8a637-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
