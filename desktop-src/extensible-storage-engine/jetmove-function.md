---
description: 'Saiba mais sobre: função JetMove'
title: Função JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164260"
---
# <a name="jetmove-function"></a><span data-ttu-id="1a2ea-103">Função JetMove</span><span class="sxs-lookup"><span data-stu-id="1a2ea-103">JetMove Function</span></span>


<span data-ttu-id="1a2ea-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1a2ea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="1a2ea-105">Função JetMove</span><span class="sxs-lookup"><span data-stu-id="1a2ea-105">JetMove Function</span></span>

<span data-ttu-id="1a2ea-106">A função **JetMove** posiciona um cursor no início ou no final de um índice e percorre as entradas nesse índice para frente ou para trás.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="1a2ea-107">Também é possível mover o cursor para frente ou para trás no índice atual por um número especificado de entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="1a2ea-108">Outra abordagem é limitar artificialmente as entradas de índice que podem ser enumeradas usando **JetMove** Configurando um intervalo de índice no cursor usando [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1a2ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a2ea-109">Parameters</span></span>

<span data-ttu-id="1a2ea-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1a2ea-110">*sesid*</span></span>

<span data-ttu-id="1a2ea-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-111">The session to use for this call.</span></span>

<span data-ttu-id="1a2ea-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1a2ea-112">*tableid*</span></span>

<span data-ttu-id="1a2ea-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-113">The cursor to use for this call.</span></span>

<span data-ttu-id="1a2ea-114">*Galinha*</span><span class="sxs-lookup"><span data-stu-id="1a2ea-114">*cRow*</span></span>

<span data-ttu-id="1a2ea-115">Um deslocamento arbitrário que indica o movimento desejado do cursor no índice atual.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="1a2ea-116">Além dos deslocamentos padrão, esse parâmetro também pode ser definido com uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a2ea-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1a2ea-117">Value</span></span></p></th>
<th><p><span data-ttu-id="1a2ea-118">Significado</span><span class="sxs-lookup"><span data-stu-id="1a2ea-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="1a2ea-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-120">Move o cursor para a primeira entrada de índice no índice (se houver).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="1a2ea-121"><strong>Observação</strong>   O valor literal de-2147483648 é usado para indicar essa opção.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="1a2ea-122">Não use esse valor como um deslocamento comum ou um comportamento não intencional pode resultar.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="1a2ea-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-124">Move o cursor para a última entrada de índice no índice (se houver).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="1a2ea-125"><strong>Observação</strong>   O valor literal de 2147483647 é usado para indicar essa opção.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="1a2ea-126">Não use esse valor como um deslocamento comum ou um comportamento não intencional pode resultar.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="1a2ea-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-128">Move o cursor para a próxima entrada de índice no índice (se houver).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="1a2ea-129">Esse valor é exatamente igual a um deslocamento comum de + 1.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1a2ea-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-131">Move o cursor para a entrada de índice anterior no índice (se houver).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="1a2ea-132">Esse valor é exatamente igual a um deslocamento comum de-1 ou 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="1a2ea-133">O cursor permanece na posição lógica atual e a existência da entrada de índice que corresponde a essa posição lógica será testada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a2ea-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1a2ea-134">*grbit*</span></span>

<span data-ttu-id="1a2ea-135">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a2ea-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1a2ea-136">Value</span></span></p></th>
<th><p><span data-ttu-id="1a2ea-137">Significado</span><span class="sxs-lookup"><span data-stu-id="1a2ea-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="1a2ea-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-139">Move o cursor para frente ou para trás pelo número de entradas de índice necessárias para ignorar o número solicitado de valores de chave de índice encontrados no índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="1a2ea-140">Isso tem o efeito de recolher entradas de índice com valores de chave duplicados em uma única entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="1a2ea-141">Normalmente, um deslocamento moverá o cursor pelo número especificado de entradas de índice, independentemente de seus valores de chave.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1a2ea-142">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1a2ea-142">Return Value</span></span>

<span data-ttu-id="1a2ea-143">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1a2ea-144">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a2ea-145">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1a2ea-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="1a2ea-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a2ea-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1a2ea-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-148">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-148">The operation completed successfully.</span></span> <span data-ttu-id="1a2ea-149">Para <strong>JetMove</strong>, isso significa que uma entrada de índice foi encontrada no local ou deslocamento solicitado no índice atual.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1a2ea-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-151">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1a2ea-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-153">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1a2ea-154"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1a2ea-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-156">O cursor não está posicionado atualmente em uma entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="1a2ea-157">Para <strong>JetMove</strong>, isso significa que uma entrada de índice não foi encontrada no local ou deslocamento solicitado no índice atual.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1a2ea-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-159">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="1a2ea-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-161">No momento, o cursor está posicionado logicamente em uma entrada de índice que corresponde a um registro que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1a2ea-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-163">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1a2ea-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-165">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1a2ea-166"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1a2ea-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1a2ea-168">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a2ea-169">Se essa função for bem sucedido, o cursor será posicionado em uma entrada de índice que corresponda ao local ou deslocamento solicitado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="1a2ea-170">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1a2ea-171">Se um intervalo de índice estiver em vigor e JET_MoveFirst ou JET_MoveLast tiver sido especificado, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="1a2ea-172">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-172">No change to the database state will occur.</span></span>

<span data-ttu-id="1a2ea-173">Se essa função falhar, a posição do cursor permanecerá inalterada, a menos que JET_errNoCurrentRecord tenha sido retornado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="1a2ea-174">Nesse caso, o cursor será posicionado onde a entrada de índice que corresponde ao local ou deslocamento solicitado teria sido.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="1a2ea-175">O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="1a2ea-176">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1a2ea-177">Se um intervalo de índice estiver em vigor e JET_MoveFirst ou JET_MoveLast tiver sido especificado, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="1a2ea-178">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1a2ea-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a2ea-179">Remarks</span></span>

<span data-ttu-id="1a2ea-180">Um cursor pode ser movido para duas posições especiais usando **JetMove**, antes da primeira e após a última.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="1a2ea-181">Se o cursor estiver na primeira entrada de índice na tabela e **JetMove** for chamado com JET_MovePrevious, a chamada falhará com JET_errNoCurrentRecord e o cursor será posicionado logicamente antes da primeira entrada no índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="1a2ea-182">Essa posição lógica é mantida mesmo que outra entrada de índice seja inserida antes da primeira entrada no índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="1a2ea-183">Uma situação análoga ocorre para o depois do último em relação ao final do índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="1a2ea-184">Antes de primeiro e depois da última, as últimas são úteis ao configurar um intervalo de entradas de índice a ser iterado usando **JetMove**, usando um modelo de iterador que espera sempre mover para o próximo elemento (ou anterior) antes de usar esse elemento.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="1a2ea-185">O conjunto de entradas de índice que podem ser visitadas por **JetMove** pode ser limitado Configurando um intervalo de índice no cursor.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="1a2ea-186">Isso é útil para aplicativos que enumeram um conjunto de entradas de índice que correspondem a critérios simples que podem ser expressos por meio de um par de chaves de pesquisa criadas para esse índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="1a2ea-187">Para obter mais informações, consulte [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="1a2ea-188">Em versões anteriores ao Windows Server 2003 SP1, há um problema no **JetMove** que ocorre em alguns casos específicos, que afeta a imposição correta de um intervalo de índice, conforme configurado pela função [JetSetIndexRange](./jetsetindexrange-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1a2ea-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="1a2ea-189">Se o cursor estiver no momento antes da primeira entrada de índice e um intervalo de índice for definido com um limite superior menor que a primeira entrada de índice, a próxima chamada para **JetMove** irá erroneamente para essa entrada de índice em vez de falhar com JET_errNoCurrentRecord, conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="1a2ea-190">O mesmo erro ocorrerá na situação análoga a partir do final do índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="1a2ea-191">Essa situação pode ocorrer em um aplicativo que configura um intervalo de índice e o navega usando um iterador que espera iniciar antes da primeira entrada de índice que é membro do conjunto de entradas a serem enumeradas, em vez de iniciar na primeira entrada de índice desse conjunto.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="1a2ea-192">Essa situação também ocorre no caso análogo, começando do final do índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="1a2ea-193">A solução alternativa é que o aplicativo Verifique manualmente se a entrada de índice adquirida está dentro do intervalo de índice, comparando a chave da entrada de índice atual (recuperada usando [JetRetrieveKey](./jetretrievekey-function.md)) com a chave que representa o final do intervalo de índice atual (recuperado usando [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="1a2ea-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="1a2ea-194">É importante ter cuidado ao passar deslocamentos computados para **JetMove**.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="1a2ea-195">Se o deslocamento calculado for menor ou igual a JET_MoveFirst, esse deslocamento deverá ser dividido em várias partes, sendo que cada uma é passada para **JetMove** separadamente, mas dentro de uma única transação para obter o efeito desejado.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="1a2ea-196">O mesmo é verdadeiro para deslocamentos maiores ou iguais a JET_MoveNext.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="1a2ea-197">É improvável que um aplicativo passe por isso no mundo real, mas é bom ter uma defesa contra esse caso, considerando a semântica muito diferente de JET_MoveFirst e JET_MoveLast de um deslocamento comum.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="1a2ea-198">Quando **JetMove** é chamado com um deslocamento muito grande, como quando o parâmetro de galinha é definido como 1000, **JetMove** atravessa todas as entradas de índice 1000 para alcançar a posição final.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="1a2ea-199">Atualmente, a API do ESE não fornece uma maneira eficiente de mover diretamente para uma determinada entrada de índice por offset sem percorrer cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1a2ea-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a2ea-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1a2ea-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1a2ea-202">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-203"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="1a2ea-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1a2ea-204">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-205"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="1a2ea-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1a2ea-206">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a2ea-207"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="1a2ea-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1a2ea-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a2ea-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1a2ea-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1a2ea-210">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1a2ea-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1a2ea-211">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1a2ea-211">See Also</span></span>

[<span data-ttu-id="1a2ea-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1a2ea-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1a2ea-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1a2ea-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1a2ea-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1a2ea-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1a2ea-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1a2ea-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1a2ea-216">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="1a2ea-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="1a2ea-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="1a2ea-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
