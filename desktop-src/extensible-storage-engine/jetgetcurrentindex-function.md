---
description: 'Saiba mais sobre: função JetGetCurrentIndex'
title: Função JetGetCurrentIndex
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785288"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="37ffc-103">Função JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="37ffc-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="37ffc-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="37ffc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="37ffc-105">Função JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="37ffc-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="37ffc-106">A função **JetGetCurrentIndex** determina o nome do índice atual de um determinado cursor.</span><span class="sxs-lookup"><span data-stu-id="37ffc-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="37ffc-107">Esse nome também é usado posteriormente para selecionar novamente esse índice como o índice atual usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="37ffc-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="37ffc-108">Ele também pode ser usado para descobrir as propriedades desse índice usando [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="37ffc-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="37ffc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37ffc-109">Parameters</span></span>

<span data-ttu-id="37ffc-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="37ffc-110">*sesid*</span></span>

<span data-ttu-id="37ffc-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="37ffc-111">The session to use for this call.</span></span>

<span data-ttu-id="37ffc-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="37ffc-112">*tableid*</span></span>

<span data-ttu-id="37ffc-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="37ffc-113">The cursor to use for this call.</span></span>

<span data-ttu-id="37ffc-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="37ffc-114">*szIndexName*</span></span>

<span data-ttu-id="37ffc-115">O buffer de saída que recebe o nome do índice atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="37ffc-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="37ffc-116">*cchIndexName*</span><span class="sxs-lookup"><span data-stu-id="37ffc-116">*cchIndexName*</span></span>

<span data-ttu-id="37ffc-117">O tamanho máximo em caracteres do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="37ffc-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="37ffc-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="37ffc-118">Return Value</span></span>

<span data-ttu-id="37ffc-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="37ffc-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="37ffc-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37ffc-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37ffc-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="37ffc-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="37ffc-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="37ffc-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="37ffc-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="37ffc-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="37ffc-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="37ffc-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="37ffc-126">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="37ffc-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="37ffc-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="37ffc-128">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="37ffc-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="37ffc-129">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="37ffc-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="37ffc-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="37ffc-131">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="37ffc-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="37ffc-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="37ffc-133">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="37ffc-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="37ffc-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="37ffc-135">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="37ffc-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="37ffc-136">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="37ffc-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="37ffc-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="37ffc-138">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="37ffc-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="37ffc-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="37ffc-140">A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber o nome inteiro do índice.</span><span class="sxs-lookup"><span data-stu-id="37ffc-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="37ffc-141">O buffer de saída foi preenchido com a maior parte do nome do índice que se ajustaria.</span><span class="sxs-lookup"><span data-stu-id="37ffc-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="37ffc-142">Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="37ffc-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="37ffc-143"><strong>Observação  </strong> Esse erro não será retornado se cchIndexName for zero.</span><span class="sxs-lookup"><span data-stu-id="37ffc-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="37ffc-144">Consulte a seção comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="37ffc-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37ffc-145">Em caso de sucesso, o nome do índice atual do cursor fornecido será retornado no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="37ffc-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="37ffc-146">Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá a maior parte do nome do índice que se ajustará no espaço fornecido.</span><span class="sxs-lookup"><span data-stu-id="37ffc-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="37ffc-147">Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres retornada nesse buffer será terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="37ffc-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="37ffc-148">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="37ffc-148">No change to the database state will occur.</span></span>

<span data-ttu-id="37ffc-149">Em caso de falha, o estado do buffer de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="37ffc-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="37ffc-150">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="37ffc-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37ffc-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="37ffc-151">Remarks</span></span>

<span data-ttu-id="37ffc-152">Se não houver um índice atual para o cursor, uma cadeia de caracteres vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="37ffc-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="37ffc-153">Isso pode acontecer quando o cursor está no índice clusterizado da tabela e nenhum índice primário foi definido.</span><span class="sxs-lookup"><span data-stu-id="37ffc-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="37ffc-154">Esse índice é conhecido como o índice sequencial da tabela e não tem definição.</span><span class="sxs-lookup"><span data-stu-id="37ffc-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="37ffc-155">Em qualquer caso, definir o índice atual como uma cadeia de caracteres vazia usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md) selecionará o índice clusterizado, independentemente da presença de uma definição de índice primário.</span><span class="sxs-lookup"><span data-stu-id="37ffc-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="37ffc-156">Há um bug importante nessa função que está presente em todas as versões.</span><span class="sxs-lookup"><span data-stu-id="37ffc-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="37ffc-157">Se o buffer de saída for muito pequeno para receber o nome inteiro do índice e o buffer de saída tiver pelo menos um caractere de comprimento, JET_wrnBufferTruncated não será retornado.</span><span class="sxs-lookup"><span data-stu-id="37ffc-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="37ffc-158">JET_errSuccess será retornado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="37ffc-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="37ffc-159">Para evitar esse problema, o buffer de saída deve ser sempre pelo menos JET_cbNameMost + 1 (65) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="37ffc-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="37ffc-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ffc-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-161"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-162">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="37ffc-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-163"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-164">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="37ffc-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-165"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-166">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="37ffc-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-167"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-168">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="37ffc-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ffc-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-170">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="37ffc-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ffc-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="37ffc-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="37ffc-172">Implementado como <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="37ffc-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="37ffc-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="37ffc-173">See Also</span></span>

[<span data-ttu-id="37ffc-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="37ffc-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="37ffc-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="37ffc-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="37ffc-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="37ffc-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="37ffc-177">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="37ffc-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="37ffc-178">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="37ffc-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
