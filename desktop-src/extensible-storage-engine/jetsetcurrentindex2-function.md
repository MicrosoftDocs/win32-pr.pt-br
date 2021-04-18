---
description: 'Saiba mais sobre: função JetSetCurrentIndex2'
title: Função JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802098"
---
# <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="046f2-103">Função JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="046f2-103">JetSetCurrentIndex2 Function</span></span>


<span data-ttu-id="046f2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="046f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="046f2-105">Função JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="046f2-105">JetSetCurrentIndex2 Function</span></span>

<span data-ttu-id="046f2-106">A função **JetSetCurrentIndex2** define o índice atual de um cursor que define quais registros em uma tabela são visíveis para esse cursor e a ordem em que aparecem, selecionando o conjunto de entradas de índice a ser usado para expor esses registros.</span><span class="sxs-lookup"><span data-stu-id="046f2-106">The **JetSetCurrentIndex2** function sets the current index of a cursor that defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="046f2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="046f2-107">Parameters</span></span>

<span data-ttu-id="046f2-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="046f2-108">*sesid*</span></span>

<span data-ttu-id="046f2-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="046f2-109">The session to use for this call.</span></span>

<span data-ttu-id="046f2-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="046f2-110">*tableid*</span></span>

<span data-ttu-id="046f2-111">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="046f2-111">The cursor to use for this call.</span></span>

<span data-ttu-id="046f2-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="046f2-112">*szIndexName*</span></span>

<span data-ttu-id="046f2-113">O nome do índice a ser selecionado para o cursor.</span><span class="sxs-lookup"><span data-stu-id="046f2-113">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="046f2-114">Se esse parâmetro for nulo ou uma cadeia de caracteres vazia, o índice clusterizado será selecionado.</span><span class="sxs-lookup"><span data-stu-id="046f2-114">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="046f2-115">Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice clusterizado.</span><span class="sxs-lookup"><span data-stu-id="046f2-115">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="046f2-116">Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado.</span><span class="sxs-lookup"><span data-stu-id="046f2-116">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="046f2-117">O índice sequencial não tem nenhuma definição de índice.</span><span class="sxs-lookup"><span data-stu-id="046f2-117">The sequential index has no index definition.</span></span> <span data-ttu-id="046f2-118">Consulte [JetCreateIndex](./jetcreateindex-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="046f2-118">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="046f2-119">Se *pIndexID* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.</span><span class="sxs-lookup"><span data-stu-id="046f2-119">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="046f2-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="046f2-120">*grbit*</span></span>

<span data-ttu-id="046f2-121">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="046f2-121">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="046f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="046f2-122">Value</span></span></p></th>
<th><p><span data-ttu-id="046f2-123">Significado</span><span class="sxs-lookup"><span data-stu-id="046f2-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="046f2-124">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="046f2-124">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="046f2-125">Essa opção indica que o cursor deve ser posicionado na primeira entrada do índice especificado.</span><span class="sxs-lookup"><span data-stu-id="046f2-125">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="046f2-126">Se o índice clusterizado estiver sendo selecionado (índice primário ou índice sequencial) e o índice atual for um índice secundário, JET_bitMoveFirst será assumido.</span><span class="sxs-lookup"><span data-stu-id="046f2-126">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="046f2-127">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="046f2-127">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-128">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="046f2-128">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="046f2-129">Essa opção indica que o cursor deve ser posicionado na entrada de índice do novo índice que corresponde ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="046f2-129">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="046f2-130">Se a definição do novo índice contiver pelo menos uma coluna de chave com valores múltiplos, a entrada do índice de destino será ambígua.</span><span class="sxs-lookup"><span data-stu-id="046f2-130">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="046f2-131">Nesse caso, o <em>itagSequence</em> especificado é usado para selecionar qual múltiplo valor da coluna de chave com valores múltiplos mais significativos é usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="046f2-131">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="046f2-132">Só é necessário passar um único <em>itagSequence</em> mesmo no caso de várias colunas de chave com valores múltiplos, pois o mecanismo expande apenas todos os valores para a coluna de chave com valores múltiplos mais significativos.</span><span class="sxs-lookup"><span data-stu-id="046f2-132">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="046f2-133">Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="046f2-133">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="046f2-134">Se JET_bitMoveFirst for especificado, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="046f2-134">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="046f2-135">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="046f2-135">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="046f2-136">Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="046f2-136">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="046f2-137">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="046f2-137">Return Value</span></span>

<span data-ttu-id="046f2-138">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="046f2-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="046f2-139">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="046f2-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="046f2-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="046f2-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="046f2-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="046f2-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="046f2-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="046f2-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="046f2-143">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="046f2-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-144">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="046f2-144">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="046f2-145">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valores múltiplos na nova definição para o índice que corresponde ao número de sequência especificado.</span><span class="sxs-lookup"><span data-stu-id="046f2-145">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new definition for the index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="046f2-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="046f2-147">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="046f2-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="046f2-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="046f2-149">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="046f2-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="046f2-150">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="046f2-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-151">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="046f2-151">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="046f2-152">O conteúdo da ID de índice não era válido ou expirou e precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="046f2-152">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="046f2-153">Isso pode ocorrer para <strong>JetSetCurrentIndex2</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="046f2-153">This can happen for <strong>JetSetCurrentIndex2</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="046f2-154">pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows Server 2003 e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="046f2-154">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="046f2-155">O mecanismo foi desligado porque a ID do índice foi buscada.</span><span class="sxs-lookup"><span data-stu-id="046f2-155">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="046f2-156">Todos os cursores que fazem referência à tabela que contém o índice correspondente à ID do índice foram fechados e o mecanismo removeu a definição do índice do cache do esquema.</span><span class="sxs-lookup"><span data-stu-id="046f2-156">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for the index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="046f2-157">A ID de índice está sendo usada com um cursor aberto na tabela incorreta.</span><span class="sxs-lookup"><span data-stu-id="046f2-157">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="046f2-158">O índice foi descartado ou ainda não está visível para a sessão.</span><span class="sxs-lookup"><span data-stu-id="046f2-158">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-159">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="046f2-159">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="046f2-160">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="046f2-160">One of the specified object names was invalid.</span></span> <span data-ttu-id="046f2-161">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="046f2-161">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="046f2-162">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="046f2-162">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="046f2-163">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="046f2-163">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="046f2-164">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="046f2-164">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="046f2-165">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="046f2-165">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="046f2-166">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="046f2-166">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="046f2-167">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="046f2-167">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="046f2-168">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="046f2-168">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="046f2-169">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="046f2-169">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="046f2-170">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="046f2-170">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-171">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="046f2-171">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="046f2-172">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="046f2-172">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="046f2-173">Isso pode ocorrer para <strong>JetSetCurrentIndex2</strong> quando <em>PINDEXID</em> não é nulo e pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows XP e versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="046f2-173">This can happen for <strong>JetSetCurrentIndex2</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-174">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="046f2-174">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="046f2-175">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="046f2-175">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-176">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="046f2-176">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="046f2-177">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="046f2-177">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-178">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="046f2-178">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="046f2-179">O mecanismo esgotou seu pool de recursos usados para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="046f2-179">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="046f2-180">O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="046f2-180">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="046f2-181">Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="046f2-181">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="046f2-182">Isso pode ocorrer para <strong>JetSetCurrentIndex2</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</span><span class="sxs-lookup"><span data-stu-id="046f2-182">This can happen for <strong>JetSetCurrentIndex2</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-183">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="046f2-183">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="046f2-184">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="046f2-184">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-185">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="046f2-185">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="046f2-186">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="046f2-186">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="046f2-187">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="046f2-187">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-188">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="046f2-188">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="046f2-189">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="046f2-189">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="046f2-190">Em caso de sucesso, o índice atual do cursor é definido como o índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="046f2-190">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="046f2-191">As entradas de índice agora podem ser buscadas usando [JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="046f2-191">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="046f2-192">As entradas de índice também podem ser enumeradas usando [JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice.</span><span class="sxs-lookup"><span data-stu-id="046f2-192">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="046f2-193">A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou em uma entrada de índice específica que está relacionada à posição atual do cursor no índice antigo (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="046f2-193">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="046f2-194">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="046f2-194">No change to the database state will occur.</span></span>

<span data-ttu-id="046f2-195">Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="046f2-195">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="046f2-196">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="046f2-196">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="046f2-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="046f2-197">Remarks</span></span>

<span data-ttu-id="046f2-198">Se a dica de ID de índice estiver obsoleta, a API simplesmente falhará.</span><span class="sxs-lookup"><span data-stu-id="046f2-198">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="046f2-199">Não há nenhum fallback para o nome de texto do índice nesse caso, como pode esperar.</span><span class="sxs-lookup"><span data-stu-id="046f2-199">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="046f2-200">Esse fallback deve ser feito manualmente pelo chamador da API.</span><span class="sxs-lookup"><span data-stu-id="046f2-200">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="046f2-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="046f2-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="046f2-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-203">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="046f2-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-204"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-205">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="046f2-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-206"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-207">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="046f2-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-208"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="046f2-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="046f2-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-211">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="046f2-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046f2-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="046f2-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="046f2-213">Implementado como <strong>JetSetCurrentIndex2W</strong> (Unicode) e <strong>JetSetCurrentIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="046f2-213">Implemented as <strong>JetSetCurrentIndex2W</strong> (Unicode) and <strong>JetSetCurrentIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="046f2-214">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="046f2-214">See Also</span></span>

[<span data-ttu-id="046f2-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="046f2-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="046f2-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="046f2-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="046f2-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="046f2-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="046f2-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="046f2-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="046f2-219">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="046f2-219">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="046f2-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="046f2-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="046f2-221">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="046f2-221">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="046f2-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="046f2-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="046f2-223">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="046f2-223">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="046f2-224">JetMove</span><span class="sxs-lookup"><span data-stu-id="046f2-224">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="046f2-225">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="046f2-225">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="046f2-226">JetSeek</span><span class="sxs-lookup"><span data-stu-id="046f2-226">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="046f2-227">JetStopService</span><span class="sxs-lookup"><span data-stu-id="046f2-227">JetStopService</span></span>](./jetstopservice-function.md)
