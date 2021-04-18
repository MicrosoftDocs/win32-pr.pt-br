---
description: 'Saiba mais sobre: função JetSetCurrentIndex3'
title: Função JetSetCurrentIndex3
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97aa356d44ab72f7cd240a42351d9962777ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785934"
---
# <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="bfeeb-103">Função JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="bfeeb-103">JetSetCurrentIndex3 Function</span></span>


<span data-ttu-id="bfeeb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bfeeb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="bfeeb-105">Função JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="bfeeb-105">JetSetCurrentIndex3 Function</span></span>

<span data-ttu-id="bfeeb-106">A função **JetSetCurrentIndex3** é usada para definir o índice atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-106">The **JetSetCurrentIndex3** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="bfeeb-107">O índice atual de um cursor define quais registros em uma tabela são visíveis para esse cursor e a ordem na qual aparecem, selecionando o conjunto de entradas de índice a ser usado para expor esses registros.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="bfeeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfeeb-108">Parameters</span></span>

<span data-ttu-id="bfeeb-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bfeeb-109">*sesid*</span></span>

<span data-ttu-id="bfeeb-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-110">The session to use for this call.</span></span>

<span data-ttu-id="bfeeb-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bfeeb-111">*tableid*</span></span>

<span data-ttu-id="bfeeb-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-112">The cursor to use for this call.</span></span>

<span data-ttu-id="bfeeb-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="bfeeb-113">*szIndexName*</span></span>

<span data-ttu-id="bfeeb-114">O nome do índice a ser selecionado para o cursor.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="bfeeb-115">Se esse parâmetro for nulo ou uma cadeia de caracteres vazia, o índice clusterizado será selecionado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="bfeeb-116">Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice clusterizado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="bfeeb-117">Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="bfeeb-118">O índice sequencial não tem nenhuma definição de índice.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-118">The sequential index has no index definition.</span></span> <span data-ttu-id="bfeeb-119">Consulte [JetCreateIndex](./jetcreateindex-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="bfeeb-120">Se *pIndexID* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="bfeeb-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bfeeb-121">*grbit*</span></span>

<span data-ttu-id="bfeeb-122">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-122">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfeeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bfeeb-123">Value</span></span></p></th>
<th><p><span data-ttu-id="bfeeb-124">Significado</span><span class="sxs-lookup"><span data-stu-id="bfeeb-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-125">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="bfeeb-125">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-126">Essa opção indica que o cursor deve ser posicionado na primeira entrada do índice especificado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-126">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="bfeeb-127">Se o índice clusterizado estiver sendo selecionado (índice primário ou índice sequencial) e o índice atual for um índice secundário, JET_bitMoveFirst será assumido.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-127">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="bfeeb-128">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-128">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-129">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="bfeeb-129">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-130">Essa opção indica que o cursor deve ser posicionado na entrada de índice do novo índice que corresponde ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-130">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="bfeeb-131">Se a definição do novo índice contiver pelo menos uma coluna de chave com valores múltiplos, a entrada do índice de destino será ambígua.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-131">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="bfeeb-132">Nesse caso, o <em>itagSequence</em> especificado é usado para selecionar qual múltiplo valor da coluna de chave com valores múltiplos mais significativos é usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-132">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="bfeeb-133">Só é necessário passar um único <em>itagSequence</em> mesmo no caso de várias colunas de chave com valores múltiplos, pois o mecanismo expande apenas todos os valores para a coluna de chave com valores múltiplos mais significativos.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-133">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="bfeeb-134">Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-134">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="bfeeb-135">Se JET_bitMoveFirst for especificado, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-135">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="bfeeb-136">Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-136">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="bfeeb-137">Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-137">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bfeeb-138">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="bfeeb-138">*itagSequence*</span></span>

<span data-ttu-id="bfeeb-139">Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-139">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="bfeeb-140">Esse parâmetro só é usado em conjunto com JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-140">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="bfeeb-141">Consulte a descrição dessa opção para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-141">See the description of this option for more details.</span></span>

<span data-ttu-id="bfeeb-142">Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-142">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="bfeeb-143">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bfeeb-143">Return Value</span></span>

<span data-ttu-id="bfeeb-144">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-144">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bfeeb-145">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-145">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfeeb-146">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bfeeb-146">Return code</span></span></p></th>
<th><p><span data-ttu-id="bfeeb-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfeeb-147">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-148">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bfeeb-148">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-149">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-149">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-150">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="bfeeb-150">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-151">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valores múltiplos na definição do novo índice que corresponde ao número de sequência especificado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-151">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-152">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bfeeb-152">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-153">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-153">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-154">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bfeeb-154">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-155">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-155">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bfeeb-156">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-157">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="bfeeb-157">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-158">O conteúdo da ID de índice não era válido ou expirou e precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-158">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="bfeeb-159">Isso pode ocorrer para <strong>JetSetCurrentIndex3</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="bfeeb-159">This can happen for <strong>JetSetCurrentIndex3</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="bfeeb-160">pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows Server 2003 e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-160">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-161">O mecanismo foi desligado porque a ID do índice foi buscada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-161">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-162">Todos os cursores que fazem referência à tabela que contém o índice correspondente à ID de índice foram fechados e o mecanismo removeu a definição desse índice do cache de esquema.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-162">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for that index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-163">A ID de índice está sendo usada com um cursor aberto na tabela incorreta.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-163">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-164">O índice foi descartado ou ainda não está visível para a sessão.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-164">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-165">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="bfeeb-165">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-166">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-166">One of the specified object names was invalid.</span></span> <span data-ttu-id="bfeeb-167">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-167">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="bfeeb-168">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="bfeeb-168">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="bfeeb-169">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-169">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-170">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-170">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-171">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-171">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-172">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-172">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-173">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-173">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-174">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-174">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="bfeeb-175">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-175">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="bfeeb-176">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-176">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-177">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bfeeb-177">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-178">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-178">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="bfeeb-179">Isso pode ocorrer para <strong>JetSetCurrentIndex3</strong> quando <em>PINDEXID</em> não é nulo e pIndexID- &gt; cbStruct não tem o tamanho esperado (Windows XP e versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-179">This can happen for <strong>JetSetCurrentIndex3</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-180">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bfeeb-180">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-181">Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-181">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-182">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bfeeb-182">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-183">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-183">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-184">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="bfeeb-184">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-185">O mecanismo esgotou seu pool de recursos usados para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-185">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="bfeeb-186">O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-186">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="bfeeb-187">Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-187">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="bfeeb-188">Isso pode ocorrer para <strong>JetSetCurrentIndex3</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-188">This can happen for <strong>JetSetCurrentIndex3</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-189">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bfeeb-189">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-190">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-190">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-191">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bfeeb-191">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-192">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-192">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="bfeeb-193">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-193">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-194">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bfeeb-194">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bfeeb-195">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-195">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bfeeb-196">Em caso de sucesso, o índice atual do cursor é definido como o índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-196">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="bfeeb-197">As entradas de índice agora podem ser buscadas usando [JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-197">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="bfeeb-198">As entradas de índice também podem ser enumeradas usando [JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-198">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="bfeeb-199">A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou em uma entrada de índice específica que está relacionada à posição atual do cursor no índice antigo (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-199">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="bfeeb-200">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-200">No change to the database state will occur.</span></span>

<span data-ttu-id="bfeeb-201">Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-201">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="bfeeb-202">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-202">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bfeeb-203">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfeeb-203">Remarks</span></span>

<span data-ttu-id="bfeeb-204">Se a dica de ID de índice estiver obsoleta, a API simplesmente falhará.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-204">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="bfeeb-205">Não há nenhum fallback para o nome de texto do índice nesse caso, como pode esperar.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-205">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="bfeeb-206">Esse fallback deve ser feito manualmente pelo chamador da API.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-206">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bfeeb-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfeeb-207">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-208"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-208"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-209">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-209">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-210"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-210"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-211">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-211">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-212"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-212"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-213">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-213">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-214"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-214"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-215">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-215">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfeeb-216"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-216"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-217">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-217">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfeeb-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bfeeb-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bfeeb-219">Implementado como <strong>JetSetCurrentIndex3W</strong> (Unicode) e <strong>JetSetCurrentIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-219">Implemented as <strong>JetSetCurrentIndex3W</strong> (Unicode) and <strong>JetSetCurrentIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bfeeb-220">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bfeeb-220">See Also</span></span>

[<span data-ttu-id="bfeeb-221">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bfeeb-221">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bfeeb-222">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bfeeb-222">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bfeeb-223">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bfeeb-223">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bfeeb-224">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bfeeb-224">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bfeeb-225">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="bfeeb-225">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="bfeeb-226">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="bfeeb-226">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="bfeeb-227">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="bfeeb-227">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="bfeeb-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="bfeeb-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="bfeeb-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="bfeeb-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="bfeeb-230">JetMove</span><span class="sxs-lookup"><span data-stu-id="bfeeb-230">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="bfeeb-231">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bfeeb-231">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="bfeeb-232">JetSeek</span><span class="sxs-lookup"><span data-stu-id="bfeeb-232">JetSeek</span></span>](./jetseek-function.md)
