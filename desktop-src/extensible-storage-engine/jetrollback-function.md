---
description: 'Saiba mais sobre: função JetRollback'
title: Função JetRollback
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764143"
---
# <a name="jetrollback-function"></a><span data-ttu-id="c933b-103">Função JetRollback</span><span class="sxs-lookup"><span data-stu-id="c933b-103">JetRollback Function</span></span>


<span data-ttu-id="c933b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c933b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="c933b-105">Função JetRollback</span><span class="sxs-lookup"><span data-stu-id="c933b-105">JetRollback Function</span></span>

<span data-ttu-id="c933b-106">A função **JetRollback** desfaz as alterações feitas no estado do banco de dados e retorna ao último ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="c933b-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="c933b-107">O **JetRollback** também fechará todos os cursores abertos durante o ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="c933b-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="c933b-108">Se o ponto de salvamento mais externo for desfeito, a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="c933b-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c933b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c933b-109">Parameters</span></span>

<span data-ttu-id="c933b-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c933b-110">*sesid*</span></span>

<span data-ttu-id="c933b-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c933b-111">The session to use for this call.</span></span>

<span data-ttu-id="c933b-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c933b-112">*grbit*</span></span>

<span data-ttu-id="c933b-113">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c933b-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c933b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c933b-114">Value</span></span></p></th>
<th><p><span data-ttu-id="c933b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c933b-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c933b-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="c933b-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="c933b-117">Essa opção solicita que todas as alterações feitas no estado do banco de dados durante todos os pontos de salvamento sejam desfeitas.</span><span class="sxs-lookup"><span data-stu-id="c933b-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="c933b-118">Como resultado, a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="c933b-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c933b-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c933b-119">Return Value</span></span>

<span data-ttu-id="c933b-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c933b-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c933b-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c933b-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c933b-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c933b-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="c933b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c933b-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c933b-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c933b-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c933b-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c933b-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c933b-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c933b-127">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c933b-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c933b-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c933b-129">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="c933b-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c933b-130">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c933b-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c933b-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c933b-132">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="c933b-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="c933b-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c933b-134">A operação falhou porque a sessão especificada não está em uma transação.</span><span class="sxs-lookup"><span data-stu-id="c933b-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c933b-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c933b-136">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="c933b-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="c933b-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="c933b-138">Não foi possível reverter as alterações devido a um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="c933b-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c933b-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c933b-140">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c933b-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c933b-141">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c933b-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c933b-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c933b-143">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="c933b-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c933b-144">Em caso de sucesso, todas as alterações feitas no banco de dados durante o ponto de salvamento atual para a sessão especificada serão desfeitas e esse ponto de salvamento será encerrado.</span><span class="sxs-lookup"><span data-stu-id="c933b-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="c933b-145">Se o último ponto de salvamento da sessão for encerrado, a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="c933b-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="c933b-146">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="c933b-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="c933b-147">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="c933b-147">No change to the database state will occur.</span></span> <span data-ttu-id="c933b-148">Uma falha durante a reversão é considerada um erro de banco de dados catastrófico.</span><span class="sxs-lookup"><span data-stu-id="c933b-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c933b-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="c933b-149">Remarks</span></span>

<span data-ttu-id="c933b-150">Deve haver uma chamada para [JetCommitTransaction](./jetcommittransaction-function.md) ou **JetRollback** para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.</span><span class="sxs-lookup"><span data-stu-id="c933b-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="c933b-151">Se os cursores foram abertos (usando [JetOpenTable](./jetopentable-function.md), por exemplo) durante um ponto de salvamento que está sendo revertido, esse cursor será fechado.</span><span class="sxs-lookup"><span data-stu-id="c933b-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c933b-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c933b-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c933b-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c933b-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c933b-154">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c933b-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c933b-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c933b-156">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c933b-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c933b-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c933b-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c933b-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c933b-159"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c933b-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c933b-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c933b-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c933b-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c933b-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c933b-162">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c933b-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c933b-163">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c933b-163">See Also</span></span>

[<span data-ttu-id="c933b-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c933b-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c933b-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c933b-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c933b-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c933b-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c933b-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="c933b-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="c933b-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="c933b-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
