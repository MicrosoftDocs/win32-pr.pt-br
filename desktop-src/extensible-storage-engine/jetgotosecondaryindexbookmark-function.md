---
description: 'Saiba mais sobre: função JetGotoSecondaryIndexBookmark'
title: Função JetGotoSecondaryIndexBookmark
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921880"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="cdff8-103">Função JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="cdff8-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="cdff8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cdff8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="cdff8-105">Função JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="cdff8-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="cdff8-106">A função **JetGotoSecondaryIndexBookmark** posiciona um cursor para uma entrada de índice que está associada ao indicador de índice secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="cdff8-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="cdff8-107">O indicador de índice secundário deve ser usado com o mesmo índice na mesma tabela da qual ele foi recuperado originalmente.</span><span class="sxs-lookup"><span data-stu-id="cdff8-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="cdff8-108">O indicador de índice secundário para uma entrada de índice pode ser recuperado usando **JetGotoSecondaryIndexBookmark**.</span><span class="sxs-lookup"><span data-stu-id="cdff8-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="cdff8-109">**Windows XP:** o **JetGotoSecondaryIndexBookmark** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="cdff8-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="cdff8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdff8-110">Parameters</span></span>

<span data-ttu-id="cdff8-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cdff8-111">*sesid*</span></span>

<span data-ttu-id="cdff8-112">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-112">The session to use for this call.</span></span>

<span data-ttu-id="cdff8-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cdff8-113">*tableid*</span></span>

<span data-ttu-id="cdff8-114">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-114">The cursor to use for this call.</span></span>

<span data-ttu-id="cdff8-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="cdff8-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="cdff8-116">O buffer que contém a chave secundária a ser usada para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="cdff8-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="cdff8-117">*cbSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="cdff8-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="cdff8-118">O tamanho da chave secundária no buffer.</span><span class="sxs-lookup"><span data-stu-id="cdff8-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="cdff8-119">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="cdff8-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="cdff8-120">O buffer que contém o indicador de chave primária a ser usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="cdff8-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="cdff8-121">*cbPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="cdff8-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="cdff8-122">O tamanho do indicador de chave primária no buffer.</span><span class="sxs-lookup"><span data-stu-id="cdff8-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="cdff8-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cdff8-123">*grbit*</span></span>

<span data-ttu-id="cdff8-124">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdff8-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdff8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cdff8-125">Value</span></span></p></th>
<th><p><span data-ttu-id="cdff8-126">Significado</span><span class="sxs-lookup"><span data-stu-id="cdff8-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="cdff8-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="cdff8-128">Caso a entrada de índice não possa mais ser encontrada, o cursor será deixado posicionado onde essa entrada de índice foi encontrada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cdff8-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="cdff8-129">A operação ainda falhará com JET_errRecordDeleted; no entanto, será possível mover para a entrada de índice seguinte ou anterior em relação à entrada de índice que agora está ausente.</span><span class="sxs-lookup"><span data-stu-id="cdff8-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cdff8-130">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cdff8-130">Return Value</span></span>

<span data-ttu-id="cdff8-131">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdff8-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cdff8-132">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cdff8-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdff8-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cdff8-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="cdff8-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdff8-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cdff8-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cdff8-136">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cdff8-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cdff8-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cdff8-138">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="cdff8-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cdff8-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cdff8-140">A operação não pode ser concluída porque o é porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="cdff8-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="cdff8-141"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cdff8-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="cdff8-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="cdff8-143">O indicador de índice secundário fornecido era inválido.</span><span class="sxs-lookup"><span data-stu-id="cdff8-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="cdff8-144">Esse erro pode ter ocorrido porque a chave secundária é zero ou o ponteiro de buffer de chave secundária é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdff8-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="cdff8-145">Esse erro ocorre porque</span><span class="sxs-lookup"><span data-stu-id="cdff8-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="cdff8-146">O índice secundário atual não tem uma restrição de exclusividade e o tamanho do indicador fornecido é zero.</span><span class="sxs-lookup"><span data-stu-id="cdff8-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="cdff8-147">O ponteiro do buffer de indicadores é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdff8-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="cdff8-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="cdff8-149">O cursor não está em um índice secundário no momento.</span><span class="sxs-lookup"><span data-stu-id="cdff8-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="cdff8-150">Não é significativo ir para um indicador de índice secundário quando o cursor não está usando um índice secundário no momento.</span><span class="sxs-lookup"><span data-stu-id="cdff8-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="cdff8-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve ser usado quando o cursor não estiver em um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="cdff8-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cdff8-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cdff8-153">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="cdff8-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="cdff8-155">Não foi possível encontrar a entrada de índice associada ao indicador de índice secundário.</span><span class="sxs-lookup"><span data-stu-id="cdff8-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cdff8-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cdff8-157">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="cdff8-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cdff8-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cdff8-159">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cdff8-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="cdff8-160"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cdff8-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cdff8-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cdff8-162">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdff8-163">Se essa função for bem sucedido, o cursor será posicionado em uma entrada de índice que está associada ao indicador de índice secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="cdff8-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="cdff8-164">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="cdff8-165">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="cdff8-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="cdff8-166">Se uma chave de pesquisa tiver sido construída para o cursor a ser usado, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="cdff8-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="cdff8-167">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="cdff8-167">No change to the database state will occur.</span></span>

<span data-ttu-id="cdff8-168">Se essa função falhar, a posição do cursor permanecerá inalterada, a menos que JET_errRecordDeleted seja retornado e JET_bitBookmarkPermitVirtualCurrency seja especificado.</span><span class="sxs-lookup"><span data-stu-id="cdff8-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="cdff8-169">Nesse caso, o cursor será posicionado onde a entrada de índice associada ao indicador de índice secundário especificado teria sido.</span><span class="sxs-lookup"><span data-stu-id="cdff8-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="cdff8-170">O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="cdff8-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="cdff8-171">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="cdff8-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="cdff8-172">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="cdff8-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="cdff8-173">Se uma chave de pesquisa tiver sido construída para o cursor a ser usado, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="cdff8-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="cdff8-174">De qualquer forma, nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="cdff8-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cdff8-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdff8-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-176"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cdff8-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cdff8-177">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cdff8-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-178"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="cdff8-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cdff8-179">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cdff8-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-180"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="cdff8-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cdff8-181">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="cdff8-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdff8-182"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="cdff8-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cdff8-183">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cdff8-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdff8-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cdff8-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cdff8-185">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cdff8-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cdff8-186">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cdff8-186">See Also</span></span>

[<span data-ttu-id="cdff8-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cdff8-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cdff8-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cdff8-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cdff8-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cdff8-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cdff8-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cdff8-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cdff8-191">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="cdff8-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="cdff8-192">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="cdff8-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="cdff8-193">JetStopService</span><span class="sxs-lookup"><span data-stu-id="cdff8-193">JetStopService</span></span>](./jetstopservice-function.md)
