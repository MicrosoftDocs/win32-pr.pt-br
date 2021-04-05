---
description: 'Saiba mais sobre: função JetSetIndexRange'
title: Função JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164632"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="b5c0e-103">Função JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b5c0e-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="b5c0e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b5c0e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="b5c0e-105">Função JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b5c0e-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="b5c0e-106">A função **JetSetIndexRange** limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e os critérios de associação especificados.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="b5c0e-107">Uma chave de pesquisa deve ter sido construída anteriormente usando [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5c0e-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b5c0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5c0e-108">Parameters</span></span>

<span data-ttu-id="b5c0e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b5c0e-109">*sesid*</span></span>

<span data-ttu-id="b5c0e-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-110">The session to use for this call.</span></span>

<span data-ttu-id="b5c0e-111">*tableidSrc*</span><span class="sxs-lookup"><span data-stu-id="b5c0e-111">*tableidSrc*</span></span>

<span data-ttu-id="b5c0e-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b5c0e-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b5c0e-113">*grbit*</span></span>

<span data-ttu-id="b5c0e-114">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b5c0e-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5c0e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b5c0e-115">Value</span></span></p></th>
<th><p><span data-ttu-id="b5c0e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b5c0e-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="b5c0e-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-118">Esta presença ou ausência dessa opção indica os critérios de limite do intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="b5c0e-119">Quando presente, essa opção indica que o limite do intervalo de índice é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="b5c0e-120">Quando ausente, essa opção indica que o limite do intervalo de índice é exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="b5c0e-121">Quando o limite do intervalo de índice é inclusivo, as entradas de índice que correspondem exatamente aos critérios de pesquisa são incluídas no intervalo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="b5c0e-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-123">Essa opção solicita que o intervalo de índice seja removido assim que tiver sido estabelecido.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="b5c0e-124">Todos os outros aspectos da operação permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="b5c0e-125">Isso é útil para testar a existência de entradas de índice que correspondam aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="b5c0e-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-127">Essa opção solicita que um intervalo de índice existente no cursor seja cancelado.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="b5c0e-128">Depois que o intervalo de índice for cancelado, será possível mover-se além do final do intervalo de índice usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="b5c0e-129">Se um intervalo de índice ainda não estiver em vigor, <strong>JetSetIndexRange</strong> falhará com JET_errInvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="b5c0e-130">Quando essa opção é especificada, todas as outras opções são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="b5c0e-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-132">Se essa opção for usada, a chave de pesquisa no cursor representará os critérios de pesquisa para a entrada de índice mais próxima do final do índice que corresponderá ao intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="b5c0e-133">O intervalo de índice será estabelecido entre a posição atual do cursor e essa entrada de índice para que todas as correspondências possam ser encontradas percorrendo o índice usando <a href="gg294117(v=exchg.10).md">JetMove</a> com JET_MoveNext ou um deslocamento positivo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="b5c0e-134">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao início do índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="b5c0e-135">Se essa opção for omitida, a chave de pesquisa no cursor representará os critérios de pesquisa para a entrada de índice mais próxima do início do índice que corresponderá ao intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="b5c0e-136">O intervalo de índice será estabelecido entre a posição atual do cursor e essa entrada de índice para que todas as correspondências possam ser encontradas com a movimentação para trás no índice usando <a href="gg294117(v=exchg.10).md">JetMove</a> com JET_MovePrevious ou um deslocamento negativo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="b5c0e-137">Não é significativo omitir essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas ao final do índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b5c0e-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b5c0e-138">Return Value</span></span>

<span data-ttu-id="b5c0e-139">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b5c0e-140">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b5c0e-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5c0e-141">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5c0e-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="b5c0e-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5c0e-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b5c0e-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-144">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="b5c0e-145">Para <strong>JetSetIndexRange</strong>, isso significa que um intervalo de índice existente foi cancelado ou que há pelo menos uma entrada de índice dentro do intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b5c0e-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-147">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b5c0e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-149">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b5c0e-150">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="b5c0e-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-152">Esse erro será retornado por <strong>JetSetIndexRange</strong> quando JET_bitRangeRemove foi especificado e nenhum intervalo de índice estava em vigor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="b5c0e-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-154">Não há uma chave de pesquisa atual para o cursor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="b5c0e-155"><strong>JetSetIndexRange</strong> exige que o cursor tenha uma chave de pesquisa válida porque usará isso para os critérios de pesquisa usados para localizar entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="b5c0e-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-157">Não há índice atual para o cursor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-157">There is no current index for the cursor.</span></span> <span data-ttu-id="b5c0e-158">Isso ocorrerá para <strong>JetSetIndexRange</strong> se o cursor estiver no índice clusterizado de uma tabela, um índice primário não foi definido.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="b5c0e-159">Não há suporte para a definição de um intervalo de índice em tal índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="b5c0e-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-161">Esse erro será retornado por <strong>JetSetIndexRange</strong> para indicar que não há entradas de índice dentro do intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b5c0e-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-163">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b5c0e-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-165">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b5c0e-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-167">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b5c0e-168">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b5c0e-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b5c0e-170">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5c0e-171">Em caso de sucesso, se JET_bitRangeRemove for especificado, o intervalo de índice que está atualmente em vigor será cancelado.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="b5c0e-172">Se JET_bitRangeRemove não for especificado e JET_bitRangeInstantDuration for especificado, nenhum intervalo de índice estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="b5c0e-173">Se nem JET_bitRangeRemove nem JET_bitRangeInstantDuration for especificado, um novo intervalo de índice estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="b5c0e-174">Esse intervalo de índice limitará temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminando na entrada de índice que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="b5c0e-175">A posição do cursor permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="b5c0e-176">Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="b5c0e-177">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-177">No change to the database state will occur.</span></span>

<span data-ttu-id="b5c0e-178">Em caso de falha, se JET_errNoCurrentRecord não for retornado, nenhum intervalo de índice estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="b5c0e-179">Se JET_errNoCurrentRecord for retornado, um novo intervalo de índice estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="b5c0e-180">Esse intervalo de índice limitará temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminando na entrada de índice que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="b5c0e-181">A posição do cursor permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="b5c0e-182">Se JET_errNoCurrentRecord for retornado e uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="b5c0e-183">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b5c0e-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5c0e-184">Remarks</span></span>

<span data-ttu-id="b5c0e-185">Um intervalo de índice é volátil e será cancelado automaticamente se qualquer navegação diferente de [JetMove](./jetmove-function.md) for executada no cursor.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="b5c0e-186">Os intervalos de índice funcionam apenas em uma direção.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="b5c0e-187">Se um limite superior for estabelecido, somente o movimento de encaminhamento usando [JetMove](./jetmove-function.md) com JET_MoveNext ou um deslocamento positivo será impedido depois que o final do intervalo de índice for atingido.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="b5c0e-188">Ainda é possível deixar o intervalo de índice nesse caso usando [JetMove](./jetmove-function.md) com JET_MovePrevious ou um deslocamento negativo.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="b5c0e-189">Uma situação análoga ocorre para um limite inferior.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b5c0e-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5c0e-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-191"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b5c0e-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c0e-192">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-193"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b5c0e-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c0e-194">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-195"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b5c0e-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c0e-196">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c0e-197"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b5c0e-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c0e-198">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c0e-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b5c0e-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c0e-200">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b5c0e-201">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b5c0e-201">See Also</span></span>

[<span data-ttu-id="b5c0e-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b5c0e-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b5c0e-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b5c0e-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b5c0e-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b5c0e-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b5c0e-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5c0e-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b5c0e-206">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b5c0e-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="b5c0e-207">JetMove</span><span class="sxs-lookup"><span data-stu-id="b5c0e-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="b5c0e-208">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b5c0e-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="b5c0e-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b5c0e-209">JetStopService</span></span>](./jetstopservice-function.md)
