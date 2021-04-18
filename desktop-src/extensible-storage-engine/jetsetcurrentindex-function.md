---
description: 'Saiba mais sobre: função JetSetCurrentIndex'
title: Função JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791455"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="a70e3-103">Função JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a70e3-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="a70e3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a70e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="a70e3-105">Função JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a70e3-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="a70e3-106">A função **JetSetCurrentIndex** pode ser usada para definir o índice atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="a70e3-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="a70e3-107">O índice atual de um cursor define quais registros em uma tabela são visíveis para esse cursor e a ordem na qual aparecem, selecionando o conjunto de entradas de índice a ser usado para expor esses registros.</span><span class="sxs-lookup"><span data-stu-id="a70e3-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="a70e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a70e3-108">Parameters</span></span>

<span data-ttu-id="a70e3-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a70e3-109">*sesid*</span></span>

<span data-ttu-id="a70e3-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a70e3-110">The session to use for this call.</span></span>

<span data-ttu-id="a70e3-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a70e3-111">*tableid*</span></span>

<span data-ttu-id="a70e3-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a70e3-112">The cursor to use for this call.</span></span>

<span data-ttu-id="a70e3-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="a70e3-113">*szIndexName*</span></span>

<span data-ttu-id="a70e3-114">O nome do índice a ser selecionado para o cursor.</span><span class="sxs-lookup"><span data-stu-id="a70e3-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="a70e3-115">Se esse parâmetro for nulo ou uma cadeia de caracteres vazia, o índice clusterizado será selecionado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="a70e3-116">Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice clusterizado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="a70e3-117">Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="a70e3-118">O índice sequencial não tem nenhuma definição de índice.</span><span class="sxs-lookup"><span data-stu-id="a70e3-118">The sequential index has no index definition.</span></span> <span data-ttu-id="a70e3-119">Consulte [JetCreateIndex](./jetcreateindex-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a70e3-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="a70e3-120">Se *pIndexID* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.</span><span class="sxs-lookup"><span data-stu-id="a70e3-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="a70e3-121">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a70e3-121">Return Value</span></span>

<span data-ttu-id="a70e3-122">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a70e3-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a70e3-123">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a70e3-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a70e3-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a70e3-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="a70e3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a70e3-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a70e3-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a70e3-127">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a70e3-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="a70e3-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="a70e3-129">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valores múltiplos na definição do novo índice que corresponde ao número de sequência especificado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a70e3-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a70e3-131">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a70e3-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="a70e3-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="a70e3-133">O conteúdo da ID de índice não era válido ou expirou e precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="a70e3-134">Isso pode ocorrer para <strong>JetSetCurrentIndex</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="a70e3-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a70e3-135">pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows Server 2003 e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="a70e3-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="a70e3-136">O mecanismo foi desligado porque a ID do índice foi buscada.</span><span class="sxs-lookup"><span data-stu-id="a70e3-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-137">Todos os cursores que fazem referência à tabela que contém o índice correspondente à ID do índice foram fechados e o mecanismo removeu a definição do índice do cache de esquema.</span><span class="sxs-lookup"><span data-stu-id="a70e3-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-138">A ID de índice está sendo usada com um cursor aberto na tabela incorreta.</span><span class="sxs-lookup"><span data-stu-id="a70e3-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-139">O índice foi descartado ou ainda não está visível para a sessão.</span><span class="sxs-lookup"><span data-stu-id="a70e3-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a70e3-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a70e3-141">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="a70e3-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a70e3-142">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a70e3-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="a70e3-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="a70e3-144">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="a70e3-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="a70e3-145">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="a70e3-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="a70e3-146">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="a70e3-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="a70e3-147">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="a70e3-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-148">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a70e3-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-149">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a70e3-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-150">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="a70e3-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-151">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="a70e3-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="a70e3-152">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="a70e3-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="a70e3-153">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="a70e3-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="a70e3-154">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="a70e3-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a70e3-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a70e3-156">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a70e3-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a70e3-157">Isso pode ocorrer para <strong>JetSetCurrentIndex</strong> quando <em>PINDEXID</em> não é nulo e pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows XP e versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="a70e3-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a70e3-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a70e3-159">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="a70e3-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a70e3-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a70e3-161">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a70e3-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a70e3-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a70e3-163">O mecanismo esgotou seu pool de recursos usados para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="a70e3-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="a70e3-164">O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="a70e3-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="a70e3-165">Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a70e3-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="a70e3-166">Isso pode ocorrer para <strong>JetSetCurrentIndex</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</span><span class="sxs-lookup"><span data-stu-id="a70e3-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a70e3-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a70e3-168">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="a70e3-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a70e3-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a70e3-170">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a70e3-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a70e3-171">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a70e3-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a70e3-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a70e3-173">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="a70e3-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a70e3-174">Em caso de sucesso, o índice atual do cursor é definido como o índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="a70e3-175">As entradas de índice agora podem ser buscadas usando [JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="a70e3-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="a70e3-176">As entradas de índice também podem ser enumeradas usando [JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice.</span><span class="sxs-lookup"><span data-stu-id="a70e3-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="a70e3-177">A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou em uma entrada de índice específica que está relacionada à posição atual do cursor no índice antigo (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="a70e3-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="a70e3-178">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a70e3-178">No change to the database state will occur.</span></span>

<span data-ttu-id="a70e3-179">Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="a70e3-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="a70e3-180">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a70e3-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a70e3-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="a70e3-181">Remarks</span></span>

<span data-ttu-id="a70e3-182">Se a dica de ID de índice estiver obsoleta, a API simplesmente falhará.</span><span class="sxs-lookup"><span data-stu-id="a70e3-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="a70e3-183">Não há nenhum fallback para o nome de texto do índice nesse caso, como pode esperar.</span><span class="sxs-lookup"><span data-stu-id="a70e3-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="a70e3-184">Esse fallback deve ser feito manualmente pelo chamador da API.</span><span class="sxs-lookup"><span data-stu-id="a70e3-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a70e3-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a70e3-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-187">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a70e3-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-188"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-189">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a70e3-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-190"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-191">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a70e3-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-192"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a70e3-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a70e3-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-195">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a70e3-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a70e3-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a70e3-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a70e3-197">Implementado como <strong>JetSetCurrentIndexW</strong> (Unicode) e <strong>JetSetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a70e3-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a70e3-198">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a70e3-198">See Also</span></span>

[<span data-ttu-id="a70e3-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a70e3-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a70e3-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a70e3-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a70e3-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a70e3-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a70e3-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a70e3-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a70e3-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="a70e3-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="a70e3-204">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="a70e3-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="a70e3-205">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a70e3-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="a70e3-206">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a70e3-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="a70e3-207">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a70e3-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="a70e3-208">JetMove</span><span class="sxs-lookup"><span data-stu-id="a70e3-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a70e3-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="a70e3-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="a70e3-210">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a70e3-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="a70e3-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a70e3-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a70e3-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a70e3-212">JetStopService</span></span>](./jetstopservice-function.md)
