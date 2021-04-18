---
description: 'Saiba mais sobre: função JetBeginTransaction3'
title: Função JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766446"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="50639-103">Função JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="50639-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="50639-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="50639-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="50639-105">A função **JetBeginTransaction3** faz com que uma sessão Insira uma transação e crie um novo ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="50639-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="50639-106">Essa função pode ser chamada mais de uma vez em uma única sessão para criar pontos de salvamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="50639-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="50639-107">Esses pontos de salvamento podem ser usados para manter ou descartar as alterações no banco de dados de forma seletiva.</span><span class="sxs-lookup"><span data-stu-id="50639-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="50639-108">A função **JetBeginTransaction3** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50639-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="50639-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50639-109">Parameters</span></span>

<span data-ttu-id="50639-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="50639-110">*sesid*</span></span>

<span data-ttu-id="50639-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="50639-111">The session to use for this call.</span></span>

<span data-ttu-id="50639-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="50639-112">*trxid*</span></span>

<span data-ttu-id="50639-113">Um identificador opcional fornecido pelo usuário para identificar a transação.</span><span class="sxs-lookup"><span data-stu-id="50639-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="50639-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="50639-114">*grbit*</span></span>

<span data-ttu-id="50639-115">Um grupo de bits que especifica zero ou mais os valores de opção de chamada listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="50639-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50639-116">Valor</span><span class="sxs-lookup"><span data-stu-id="50639-116">Value</span></span></p></th>
<th><p><span data-ttu-id="50639-117">Significado</span><span class="sxs-lookup"><span data-stu-id="50639-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50639-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="50639-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="50639-119">A transação não modificará o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50639-119">The transaction will not modify the database.</span></span> <span data-ttu-id="50639-120">Se uma atualização for tentada, essa operação falhará com JET_errTransReadOnly código de resposta.</span><span class="sxs-lookup"><span data-stu-id="50639-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="50639-121">Essa opção é ignorada a menos que seja solicitada quando a sessão especificada ainda não estiver em uma transação.</span><span class="sxs-lookup"><span data-stu-id="50639-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="50639-122">Essa opção está disponível em versões do sistema operacional Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50639-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="50639-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50639-123">Return value</span></span>

<span data-ttu-id="50639-124">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="50639-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="50639-125">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="50639-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50639-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="50639-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="50639-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="50639-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50639-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="50639-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="50639-129">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="50639-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="50639-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="50639-131">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="50639-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50639-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="50639-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="50639-133">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="50639-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="50639-134">Esse código de retorno é retornado pelas versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50639-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="50639-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="50639-136">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="50639-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50639-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="50639-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="50639-138">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="50639-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="50639-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="50639-140">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="50639-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="50639-141">Esse erro é retornado pelas versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50639-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50639-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="50639-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="50639-143">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="50639-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="50639-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="50639-145">Uma nova transação não pode ser iniciada porque a sessão já está na profundidade máxima de ponto de salvamento permitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50639-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50639-146">Em caso de sucesso, a sessão fornecida estará dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="50639-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="50639-147">Se a sessão estava anteriormente dentro de uma transação, um novo ponto de salvamento será criado.</span><span class="sxs-lookup"><span data-stu-id="50639-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="50639-148">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="50639-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="50639-149">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="50639-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50639-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="50639-150">Remarks</span></span>

<span data-ttu-id="50639-151">Para obter mais informações sobre como as transações funcionam, consulte [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="50639-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="50639-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50639-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50639-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="50639-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="50639-154">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50639-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="50639-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="50639-156">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="50639-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50639-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="50639-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="50639-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="50639-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50639-159"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="50639-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="50639-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="50639-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50639-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="50639-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="50639-162">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="50639-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="50639-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="50639-163">See also</span></span>

[<span data-ttu-id="50639-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="50639-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="50639-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="50639-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="50639-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="50639-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="50639-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="50639-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="50639-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="50639-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="50639-169">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="50639-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="50639-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="50639-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="50639-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="50639-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="50639-172">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="50639-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="50639-173">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="50639-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
