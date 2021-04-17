---
description: 'Saiba mais sobre: função JetBeginTransaction2'
title: Função JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790317"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="5f514-103">Função JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="5f514-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="5f514-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f514-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="5f514-105">Função JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="5f514-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="5f514-106">A função **JetBeginTransaction2** faz com que uma sessão Insira uma transação e crie um novo ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="5f514-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="5f514-107">Essa função pode ser chamada mais de uma vez em uma única sessão para criar pontos de salvamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="5f514-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="5f514-108">Esses pontos de salvamento podem ser usados para manter ou descartar as alterações no banco de dados de forma seletiva.</span><span class="sxs-lookup"><span data-stu-id="5f514-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5f514-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f514-109">Parameters</span></span>

<span data-ttu-id="5f514-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5f514-110">*sesid*</span></span>

<span data-ttu-id="5f514-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5f514-111">The session to use for this call.</span></span>

<span data-ttu-id="5f514-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5f514-112">*grbit*</span></span>

<span data-ttu-id="5f514-113">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f514-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f514-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5f514-114">Value</span></span></p></th>
<th><p><span data-ttu-id="5f514-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5f514-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f514-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="5f514-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5f514-117">A transação não modificará o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5f514-117">The transaction will not modify the database.</span></span> <span data-ttu-id="5f514-118">Se uma atualização for tentada, essa operação falhará com JET_errTransReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5f514-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="5f514-119">Essa opção é ignorada a menos que seja solicitada quando a sessão especificada ainda não estiver em uma transação.</span><span class="sxs-lookup"><span data-stu-id="5f514-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="5f514-120">Essa opção só está disponível no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f514-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5f514-121">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5f514-121">Return Value</span></span>

<span data-ttu-id="5f514-122">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f514-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5f514-123">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5f514-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f514-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f514-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="5f514-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f514-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f514-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5f514-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5f514-127">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5f514-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5f514-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5f514-129">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5f514-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f514-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5f514-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5f514-131">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="5f514-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5f514-132">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5f514-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5f514-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5f514-134">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="5f514-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f514-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5f514-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5f514-136">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="5f514-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5f514-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5f514-138">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="5f514-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="5f514-139">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5f514-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f514-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5f514-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5f514-141">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="5f514-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="5f514-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="5f514-143">Uma nova transação não pode ser iniciada porque a sessão já está na profundidade máxima de ponto de salvamento permitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5f514-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f514-144">Em caso de sucesso, a sessão fornecida estará dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="5f514-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="5f514-145">Se a sessão estava anteriormente dentro de uma transação, um novo ponto de salvamento será criado.</span><span class="sxs-lookup"><span data-stu-id="5f514-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="5f514-146">Se houver falha, o estado transacional da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="5f514-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="5f514-147">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="5f514-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5f514-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f514-148">Remarks</span></span>

<span data-ttu-id="5f514-149">Para obter mais informações sobre como as transações funcionam, consulte [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="5f514-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5f514-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f514-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f514-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5f514-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f514-152">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5f514-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-153"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5f514-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f514-154">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5f514-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f514-155"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5f514-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f514-156">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5f514-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f514-157"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5f514-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5f514-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5f514-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f514-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5f514-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5f514-160">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5f514-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5f514-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5f514-161">See Also</span></span>

[<span data-ttu-id="5f514-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5f514-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5f514-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5f514-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5f514-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5f514-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5f514-165">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="5f514-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="5f514-166">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="5f514-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="5f514-167">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="5f514-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="5f514-168">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="5f514-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="5f514-169">JetRollback</span><span class="sxs-lookup"><span data-stu-id="5f514-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="5f514-170">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="5f514-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="5f514-171">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="5f514-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
