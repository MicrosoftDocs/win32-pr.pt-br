---
description: 'Saiba mais sobre: função JetGetLS'
title: Função JetGetLS
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766414"
---
# <a name="jetgetls-function"></a><span data-ttu-id="5ed51-103">Função JetGetLS</span><span class="sxs-lookup"><span data-stu-id="5ed51-103">JetGetLS Function</span></span>


<span data-ttu-id="5ed51-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5ed51-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="5ed51-105">Função JetGetLS</span><span class="sxs-lookup"><span data-stu-id="5ed51-105">JetGetLS Function</span></span>

<span data-ttu-id="5ed51-106">A função **JetGetLS** permite que o aplicativo recupere o identificador de contexto conhecido como armazenamento local que está associado a um cursor ou à tabela associada a esse cursor.</span><span class="sxs-lookup"><span data-stu-id="5ed51-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="5ed51-107">Esse identificador de contexto deve ter sido definido anteriormente usando [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ed51-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="5ed51-108">**JetGetLS** também pode ser usado para buscar simultaneamente o identificador de contexto atual para um cursor ou uma tabela e redefinir esse identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="5ed51-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="5ed51-109">**Windows XP: o JetGetLS** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ed51-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5ed51-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ed51-110">Parameters</span></span>

<span data-ttu-id="5ed51-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5ed51-111">*sesid*</span></span>

<span data-ttu-id="5ed51-112">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-112">The session to use for this call.</span></span>

<span data-ttu-id="5ed51-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5ed51-113">*tableid*</span></span>

<span data-ttu-id="5ed51-114">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-114">The cursor to use for this call.</span></span>

<span data-ttu-id="5ed51-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="5ed51-115">*pls*</span></span>

<span data-ttu-id="5ed51-116">O buffer de saída que recebe o identificador de contexto atualmente associado ao cursor ou à tabela.</span><span class="sxs-lookup"><span data-stu-id="5ed51-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="5ed51-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5ed51-117">*grbit*</span></span>

<span data-ttu-id="5ed51-118">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ed51-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ed51-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed51-119">Value</span></span></p></th>
<th><p><span data-ttu-id="5ed51-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5ed51-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="5ed51-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="5ed51-122">Indica que o identificador de contexto associado ao cursor fornecido deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5ed51-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="5ed51-123">Se nem JET_bitLSCursor nem JET_bitLSTable forem especificadas, JET_bitLSCursor será presumido.</span><span class="sxs-lookup"><span data-stu-id="5ed51-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="5ed51-124">Esta opção não pode ser usada com JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="5ed51-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="5ed51-125">A operação falhará com JET_errInvalidgrbit se for tentada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="5ed51-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="5ed51-127">Indica que o identificador de contexto associado à tabela que contém o cursor fornecido deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5ed51-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="5ed51-128">É ilegal usar essa opção com JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="5ed51-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="5ed51-129">A operação falhará com JET_errInvalidgrbit se for tentada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="5ed51-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="5ed51-131">Indica que o identificador de contexto para o objeto escolhido deve ser redefinido para JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="5ed51-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="5ed51-132">O valor atual do identificador de contexto é retornado no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="5ed51-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5ed51-133">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5ed51-133">Return Value</span></span>

<span data-ttu-id="5ed51-134">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ed51-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5ed51-135">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5ed51-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ed51-136">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5ed51-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="5ed51-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed51-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5ed51-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5ed51-139">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5ed51-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5ed51-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5ed51-141">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5ed51-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5ed51-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5ed51-143">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="5ed51-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5ed51-144">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5ed51-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5ed51-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5ed51-146">Uma das opções solicitadas era inválida, usada de maneira ilegal ou não implementada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="5ed51-147">Isso pode ocorrer para <strong>JetGetLS</strong> quando JET_bitLSCursor e JET_bitLSTable são definidos.</span><span class="sxs-lookup"><span data-stu-id="5ed51-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="5ed51-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="5ed51-149">O identificador de contexto não pôde ser retornado porque nenhum identificador de contexto está associado no momento ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="5ed51-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="5ed51-150"><strong>Observação  </strong> Esse erro não será retornado se JET_bitLSReset for especificado, mas nenhum identificador de contexto foi associado ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="5ed51-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5ed51-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5ed51-152">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5ed51-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5ed51-154">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="5ed51-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5ed51-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5ed51-156">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="5ed51-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ed51-157">Em caso de sucesso, o identificador de contexto foi recuperado com êxito do objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="5ed51-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="5ed51-158">Se JET_bitLSReset tiver sido especificado, esse identificador de contexto também foi removido com êxito do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ed51-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="5ed51-159">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="5ed51-159">No change to the database state will occur.</span></span>

<span data-ttu-id="5ed51-160">Em caso de falha, nenhuma alteração no estado do objeto solicitado ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5ed51-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="5ed51-161">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="5ed51-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5ed51-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed51-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5ed51-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed51-164">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ed51-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-165"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5ed51-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed51-166">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5ed51-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-167"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5ed51-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed51-168">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5ed51-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed51-169"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5ed51-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed51-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5ed51-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed51-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5ed51-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed51-172">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5ed51-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5ed51-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5ed51-173">See Also</span></span>

[<span data-ttu-id="5ed51-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5ed51-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5ed51-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5ed51-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5ed51-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="5ed51-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="5ed51-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5ed51-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5ed51-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5ed51-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5ed51-179">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="5ed51-179">JetSetLS</span></span>](./jetsetls-function.md)
