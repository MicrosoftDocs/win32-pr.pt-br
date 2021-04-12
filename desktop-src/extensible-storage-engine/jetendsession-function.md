---
description: 'Saiba mais sobre: função JetEndSession'
title: Função JetEndSession
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296982"
---
# <a name="jetendsession-function"></a><span data-ttu-id="75c3b-103">Função JetEndSession</span><span class="sxs-lookup"><span data-stu-id="75c3b-103">JetEndSession Function</span></span>


<span data-ttu-id="75c3b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75c3b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="75c3b-105">Função JetEndSession</span><span class="sxs-lookup"><span data-stu-id="75c3b-105">JetEndSession Function</span></span>

<span data-ttu-id="75c3b-106">A função **JetEndSession** encerra a sessão e limpa e desaloca todos os recursos associados à sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="75c3b-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="75c3b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c3b-107">Parameters</span></span>

<span data-ttu-id="75c3b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="75c3b-108">*sesid*</span></span>

<span data-ttu-id="75c3b-109">A sessão a ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="75c3b-109">The session to end.</span></span> <span data-ttu-id="75c3b-110">Os recursos associados são liberados quando a sessão termina.</span><span class="sxs-lookup"><span data-stu-id="75c3b-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="75c3b-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="75c3b-111">*grbit*</span></span>

<span data-ttu-id="75c3b-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="75c3b-112">Reserved.</span></span> <span data-ttu-id="75c3b-113">Esse parâmetro pode conter o sinalizador JET_bitForceSessionClosed, mas esse sinalizador é reservado e a configuração não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="75c3b-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="75c3b-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="75c3b-114">Return Value</span></span>

<span data-ttu-id="75c3b-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="75c3b-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="75c3b-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75c3b-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75c3b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="75c3b-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="75c3b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="75c3b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75c3b-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75c3b-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="75c3b-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="75c3b-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="75c3b-122">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="75c3b-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="75c3b-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="75c3b-124">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="75c3b-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="75c3b-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="75c3b-126">A sessão não era uma sessão JET válida.</span><span class="sxs-lookup"><span data-stu-id="75c3b-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="75c3b-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="75c3b-128">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="75c3b-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="75c3b-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="75c3b-130">A operação falhou porque não foi possível alocar memória.</span><span class="sxs-lookup"><span data-stu-id="75c3b-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="75c3b-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="75c3b-132">Isso significa que a sessão estava em uso em outro thread ou a sessão não foi definida ou redefinida corretamente.</span><span class="sxs-lookup"><span data-stu-id="75c3b-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="75c3b-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="75c3b-134">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="75c3b-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="75c3b-135">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="75c3b-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="75c3b-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="75c3b-137">Erro do sistema que indica que não há mais buffers.</span><span class="sxs-lookup"><span data-stu-id="75c3b-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="75c3b-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="75c3b-139">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="75c3b-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="75c3b-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="75c3b-141">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="75c3b-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75c3b-142">Em caso de sucesso, o identificador de sessão é fechado e não está disponível e todos os recursos relacionados a essa sessão são limpos.</span><span class="sxs-lookup"><span data-stu-id="75c3b-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="75c3b-143">Em caso de falha, há vários erros adicionais que podem ocorrer como parte do fechamento da tabela de classificação, fechamento do cursor e reversão da transação.</span><span class="sxs-lookup"><span data-stu-id="75c3b-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="75c3b-144">Esses erros são bastante improvável e extremamente improvável se suas sessões não estiverem totalmente em uso quando **JetEndSession** for chamado.</span><span class="sxs-lookup"><span data-stu-id="75c3b-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="75c3b-145">Esses erros serão retornados se alguma parte da sessão não puder ser limpa corretamente.</span><span class="sxs-lookup"><span data-stu-id="75c3b-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="75c3b-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c3b-146">Remarks</span></span>

<span data-ttu-id="75c3b-147">Essa API reverterá todas as transações abertas (não confirmadas no nível 0).</span><span class="sxs-lookup"><span data-stu-id="75c3b-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="75c3b-148">Além disso, todos os cursores associados a essa sessão e quaisquer tabelas de classificação que foram criadas ou abertas serão limpos.</span><span class="sxs-lookup"><span data-stu-id="75c3b-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="75c3b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c3b-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="75c3b-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75c3b-151">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="75c3b-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-152"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="75c3b-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75c3b-153">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="75c3b-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-154"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="75c3b-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75c3b-155">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="75c3b-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c3b-156"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="75c3b-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="75c3b-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75c3b-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c3b-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="75c3b-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="75c3b-159">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75c3b-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75c3b-160">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="75c3b-160">See Also</span></span>

[<span data-ttu-id="75c3b-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75c3b-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75c3b-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="75c3b-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="75c3b-163">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="75c3b-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="75c3b-164">JetRollback</span><span class="sxs-lookup"><span data-stu-id="75c3b-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="75c3b-165">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="75c3b-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="75c3b-166">JetStopService</span><span class="sxs-lookup"><span data-stu-id="75c3b-166">JetStopService</span></span>](./jetstopservice-function.md)
