---
description: 'Saiba mais sobre: função JetSetCurrentIndex4'
title: Função JetSetCurrentIndex4
TOCTitle: JetSetCurrentIndex4 Function
ms:assetid: 6076d02c-5701-4021-ba0a-da36bff166d1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269262(v=EXCHG.10)
ms:contentKeyID: 32765564
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex4W
- JetSetCurrentIndex4A
- JetSetCurrentIndex4
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 234b945e9ebe4421d348eab0e72556b544578b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802097"
---
# <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="9d2b2-103">Função JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="9d2b2-103">JetSetCurrentIndex4 Function</span></span>


<span data-ttu-id="9d2b2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9d2b2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex4-function"></a><span data-ttu-id="9d2b2-105">Função JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="9d2b2-105">JetSetCurrentIndex4 Function</span></span>

<span data-ttu-id="9d2b2-106">A função **JetSetCurrentIndex4** é usada para definir o índice atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-106">The **JetSetCurrentIndex4** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="9d2b2-107">O índice atual de um cursor define quais registros em uma tabela são visíveis para esse cursor e a ordem na qual aparecem, selecionando o conjunto de entradas de índice a ser usado para expor esses registros.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex4(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in_opt      JET_INDEXID* pindexid,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="9d2b2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d2b2-108">Parameters</span></span>

<span data-ttu-id="9d2b2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-109">*sesid*</span></span>

<span data-ttu-id="9d2b2-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-110">The session to use for this call.</span></span>

<span data-ttu-id="9d2b2-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-111">*tableid*</span></span>

<span data-ttu-id="9d2b2-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-112">The cursor to use for this call.</span></span>

<span data-ttu-id="9d2b2-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-113">*szIndexName*</span></span>

<span data-ttu-id="9d2b2-114">O nome do índice a ser selecionado para o cursor.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-114">The name of the index to be selected for the cursor.</span></span> <span data-ttu-id="9d2b2-115">Se esse parâmetro for nulo ou uma cadeia de caracteres vazia, o índice clusterizado será selecionado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="9d2b2-116">Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice clusterizado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="9d2b2-117">Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="9d2b2-118">O índice sequencial não tem nenhuma definição de índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-118">The sequential index has no index definition.</span></span> <span data-ttu-id="9d2b2-119">Consulte [JetCreateIndex](./jetcreateindex-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="9d2b2-120">Se *pIndexID* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="9d2b2-121">*pindexid*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-121">*pindexid*</span></span>

<span data-ttu-id="9d2b2-122">A ID do índice a ser selecionado para o cursor.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-122">The ID of the index to be selected for the cursor.</span></span>

<span data-ttu-id="9d2b2-123">A ID do índice é um identificador volátil e opaco que pode ser usado para selecionar rapidamente um índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-123">The index ID is a volatile, opaque handle that can be used to quickly select an index.</span></span> <span data-ttu-id="9d2b2-124">Essa ID pode ser recuperada usando JetGetIndexInfo ou JetGetTableIndexInfo usando a opção JET_IdxInfoIndexId.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-124">This ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo using the JET_IdxInfoIndexId option.</span></span>

<span data-ttu-id="9d2b2-125">Se *pIndexID* for NULL, o índice será selecionado pelo nome do índice e a ID do índice será ignorada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-125">If *pindexid* is NULL then the index will be selected by its index name and the index ID will be ignored.</span></span>

<span data-ttu-id="9d2b2-126">Quando esse parâmetro não estiver presente, seu valor será presumido como nulo.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="9d2b2-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-127">*grbit*</span></span>

<span data-ttu-id="9d2b2-128">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-128">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d2b2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9d2b2-129">Value</span></span></p></th>
<th><p><span data-ttu-id="9d2b2-130">Significado</span><span class="sxs-lookup"><span data-stu-id="9d2b2-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-131">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="9d2b2-131">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-132">Essa opção indica que o cursor deve ser posicionado na primeira entrada do índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-132">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="9d2b2-133">Se o índice clusterizado estiver sendo selecionado (índice primário ou índice sequencial) e o índice atual for um índice secundário, JET_bitMoveFirst será assumido.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-133">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="9d2b2-134">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-134">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-135">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="9d2b2-135">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-136">Essa opção indica que o cursor deve ser posicionado na entrada de índice do novo índice que corresponde ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-136">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="9d2b2-137">Se a definição do novo índice contiver pelo menos uma coluna de chave com valores múltiplos, a entrada do índice de destino será ambígua.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-137">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="9d2b2-138">Nesse caso, o <em>itagSequence</em> especificado é usado para selecionar qual múltiplo valor da coluna de chave com valores múltiplos mais significativos é usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-138">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="9d2b2-139">Só é necessário passar um único <em>itagSequence</em> mesmo no caso de várias colunas de chave com valores múltiplos, pois o mecanismo expande apenas todos os valores para a coluna de chave com valores múltiplos mais significativos.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-139">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="9d2b2-140">Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-140">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="9d2b2-141">Se JET_bitMoveFirst for especificado, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-141">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="9d2b2-142">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-142">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="9d2b2-143">Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-143">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d2b2-144">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="9d2b2-144">*itagSequence*</span></span>

<span data-ttu-id="9d2b2-145">Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-145">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="9d2b2-146">Esse parâmetro só é usado em conjunto com JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-146">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="9d2b2-147">Consulte a descrição dessa opção para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-147">See the description of this option for more details.</span></span>

<span data-ttu-id="9d2b2-148">Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-148">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="9d2b2-149">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9d2b2-149">Return Value</span></span>

<span data-ttu-id="9d2b2-150">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-150">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9d2b2-151">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-151">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d2b2-152">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9d2b2-152">Return code</span></span></p></th>
<th><p><span data-ttu-id="9d2b2-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d2b2-153">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-154">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9d2b2-154">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-155">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-155">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-156">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="9d2b2-156">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-157">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valores múltiplos na definição do novo índice que corresponde ao número de sequência especificado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-157">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the definition for the new index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-158">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9d2b2-158">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-159">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-159">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9d2b2-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-161">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9d2b2-162">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-163">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="9d2b2-163">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-164">O conteúdo da ID de índice não era válido ou expirou e precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-164">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="9d2b2-165">Isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="9d2b2-165">This can happen for <strong>JetSetCurrentIndex4</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d2b2-166">pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows Server 2003 e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-166">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-167">O mecanismo foi desligado porque a ID do índice foi buscada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-167">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-168">Todos os cursores que fazem referência à tabela que contém o índice correspondente à ID do índice foram fechados e o mecanismo removeu a definição do índice do cache de esquema.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-168">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-169">A ID de índice está sendo usada com um cursor aberto na tabela incorreta.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-169">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-170">O índice foi descartado ou ainda não está visível para a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-170">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-171">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9d2b2-171">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-172">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-172">One of the specified object names was invalid.</span></span> <span data-ttu-id="9d2b2-173">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-173">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="9d2b2-174">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="9d2b2-174">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d2b2-175">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-175">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-176">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-176">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-177">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-177">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-178">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-178">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-179">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-179">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-180">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-180">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="9d2b2-181">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-181">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="9d2b2-182">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-182">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-183">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9d2b2-183">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-184">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-184">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="9d2b2-185">Isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando <em>PINDEXID</em> não é nulo e pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows XP e versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-185">This can happen for <strong>JetSetCurrentIndex4</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-186">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9d2b2-186">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-187">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-187">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-188">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9d2b2-188">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-189">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-189">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-190">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="9d2b2-190">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-191">O mecanismo esgotou seu pool de recursos usados para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-191">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="9d2b2-192">O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-192">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="9d2b2-193">Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-193">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="9d2b2-194">Isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-194">This can happen for <strong>JetSetCurrentIndex4</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-195">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9d2b2-195">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-196">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-196">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-197">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9d2b2-197">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-198">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-198">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9d2b2-199">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-200">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9d2b2-200">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d2b2-201">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-201">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d2b2-202">Em caso de sucesso, o índice atual do cursor é definido como o índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-202">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="9d2b2-203">As entradas de índice agora podem ser buscadas usando [JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-203">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="9d2b2-204">As entradas de índice também podem ser enumeradas usando [JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-204">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="9d2b2-205">A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou em uma entrada de índice específica que está relacionada à posição atual do cursor no índice antigo (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-205">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="9d2b2-206">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-206">No change to the database state will occur.</span></span>

<span data-ttu-id="9d2b2-207">Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-207">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="9d2b2-208">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-208">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9d2b2-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d2b2-209">Remarks</span></span>

<span data-ttu-id="9d2b2-210">Se a dica de ID de índice estiver obsoleta, a API simplesmente falhará.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-210">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="9d2b2-211">Não há nenhum fallback para o nome de texto do índice nesse caso, como pode esperar.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-211">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="9d2b2-212">Esse fallback deve ser feito manualmente pelo chamador da API.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-212">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9d2b2-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d2b2-213">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-214"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-214"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-215">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-215">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-216"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-216"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-217">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-217">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-218"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-218"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-219">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-219">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-220"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-220"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-221">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-221">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d2b2-222"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-222"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-223">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9d2b2-223">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d2b2-224"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9d2b2-224"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9d2b2-225">Implementado como <strong>JetSetCurrentIndex4W</strong> (Unicode) e <strong>JetSetCurrentIndex4A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9d2b2-225">Implemented as <strong>JetSetCurrentIndex4W</strong> (Unicode) and <strong>JetSetCurrentIndex4A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9d2b2-226">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9d2b2-226">See Also</span></span>

[<span data-ttu-id="9d2b2-227">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9d2b2-227">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9d2b2-228">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9d2b2-228">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9d2b2-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9d2b2-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9d2b2-230">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9d2b2-230">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9d2b2-231">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="9d2b2-231">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="9d2b2-232">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="9d2b2-232">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="9d2b2-233">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="9d2b2-233">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="9d2b2-234">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9d2b2-234">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9d2b2-235">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9d2b2-235">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="9d2b2-236">JetMove</span><span class="sxs-lookup"><span data-stu-id="9d2b2-236">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="9d2b2-237">JetSeek</span><span class="sxs-lookup"><span data-stu-id="9d2b2-237">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="9d2b2-238">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9d2b2-238">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
